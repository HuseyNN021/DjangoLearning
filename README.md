# DjangoLearning
First touch to Django

<h1>Day 1</h1>
<h2>Introduction</h2>

<strong>🔹 Django nədir?
</strong>

Django Python əsaslı web framework-dür.
Web tətbiqləri (backend) yaratmaq üçün istifadə olunur.

<strong>
🔹 Virtual Environment (venv)
</strong>

Django quraşdırmazdan əvvəl virtual environment yaratmaq tövsiyə olunur.

Virtual environment (venv):

Layihəyə xüsusi Python mühiti yaradır

Paketlər sistemə yox, yalnız layihəyə yüklənir

Layihə silindikdə sistemə təsir etmir

python -m venv myenv


Aktivləşdirmə:

Windows:

source myenv/Scripts/activate


Mac/Linux:

source myenv/bin/activate

<strong>
🔹 Django project yaratmaq
</strong>
django-admin startproject examples


Bu zaman aşağıdakı fayllar yaranır:

📁 __init__.py

Qovluğun Python package olduğunu bildirir

Boş ola bilər

Import üçün lazımdır

⚙️ settings.py

Layihənin bütün konfiqurasiyası burada saxlanılır.

Əsas hissələr:
🔸 BASE_DIR
BASE_DIR = Path(__file__).resolve().parent.parent


Layihənin əsas (root) qovluğunu göstərir.

🔸 SECRET_KEY

Şifrələmə üçün istifadə olunur

Session, cookie, CSRF üçün vacibdir

GitHub-a açıq şəkildə göndərilməməlidir

.env faylında saxlanılır:

SECRET_KEY=django-insecure-...

🔸 DEBUG
DEBUG = True


True → development (xətalar görünür)

False → production (xətalar gizlədilir)

🔸 ALLOWED_HOSTS

Hansı domainlərin serverə daxil ola biləcəyini göstərir

Production-da mütləq doldurulmalıdır

🔸 INSTALLED_APPS

Burada:

Django built-in app-ləri

Custom app-lər

Xarici library-lər qeyd olunur

🔸 MIDDLEWARE

Request → Response arasında işləyən qatdır
Security, session, auth kimi işləri görür

🔸 TEMPLATES

HTML template-lərin harada yerləşdiyini göstərir

🌐 urls.py

URL-ləri view-lərə bağlayır (routing)

🚀 ASGI vs WSGI
ASGI	WSGI
Async	Sync
WebSocket dəstəyi	WebSocket yoxdur
Real-time tətbiqlər	Klassik serverlər
🔐 .env və .gitignore

.env → gizli məlumatlar (SECRET_KEY, DEBUG)

.gitignore → .env, myenv, db.sqlite3 GitHub-a getməsin deyə
