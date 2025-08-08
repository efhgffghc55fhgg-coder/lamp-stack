# lamp-stack
install lamp stack 
المشروع ده عبارة عن بلاي بوك أنسيبل بيعمل نشر أوتوماتيك للـ LAMP Stack (Linux + Apache + MySQL + PHP) مع تظبيط الفايروول.

playbook.yml: البلاي بوك الرئيسي اللي بيستدعي الـ roles بالترتيب: Apache → PHP → MySQL → Firewall.

inventories/dev/inventory: ملف بيحدد السيرفر المستهدف (IP + يوزر SSH + مفتاح الدخول).

roles:

apache: بينزل Apache، يرفع صفحة index.php، ويعمل هاندلر لإعادة تشغيله.

php: بينزل PHP والموديولات المطلوبة.

mysql: بينزل MySQL، يضبط باسورد الرووت، ويحذف اليوزرات والداتابيز الافتراضية.

firewall: بينزل UFW ويفتح بورتات SSH, HTTP, HTTPS.


vars/var.yaml: فيه المتغيرات زي باسورد MySQL.

ansible.cfg: إعدادات أنسيبل (مسار الإنفنتوري، صلاحيات، إلخ).


باختصار: ده سيستم كامل يثبت ويضبط LAMP على أي سيرفر Ubuntu بضغطة واحدة.
