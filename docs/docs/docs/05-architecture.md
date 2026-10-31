# معماری سامانه | System Architecture

## Proposed architecture / معماری پیشنهادی
A conventional Django web application is proposed for the first version.

- **Presentation layer:** Django templates, HTML, CSS, Bootstrap, JavaScript
- **Application layer:** Django views, forms, authentication, authorization, business rules
- **Domain/data layer:** Django models and ORM
- **Database:** SQLite for local development; PostgreSQL if deployment or course requirements justify it
- **Tests:** Django test framework

## Logical modules
1. Accounts and roles
2. Gym and facilities
3. Athletes and trainers
4. Exercise library
5. Workout plans and plan items
6. Nutrition plans
7. Memberships and payments
8. Reports

## Security principles
- Use Django's authentication rather than custom password storage.
- Enforce permissions on the server.
- Validate all input on the server.
- Keep secrets in environment variables and out of Git.
- Use CSRF protection and secure production settings.
- Do not store payment card details; the first version records payment metadata only.
- Use synthetic data in development and screenshots.

## فارسی
این معماری پیشنهادی است و پس از انتخاب نهایی فناوری و بررسی نیازهای استاد تثبیت می‌شود. در نسخه اول، معماری یکپارچه و ماژولار برای گروه دانشجویی ساده‌تر از معماری چندخدمتی است. ماژول‌ها جدا نگه داشته می‌شوند، اما لازم نیست هرکدام یک سرویس مستقل باشند.

## Deployment note
Local development setup is not the same as production deployment. Before public deployment, configure `DEBUG=False`, allowed hosts, HTTPS, secret management, database backups, static/media files, and production security settings.
