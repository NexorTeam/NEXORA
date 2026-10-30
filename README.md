# NEXORA | سامانه مدیریت هوشمند باشگاه‌های ورزشی
**Smart Gym Management System**

> پروژه دانشگاهی گروه NEXORA — نسخه مستندات اولیه / Initial documentation baseline

## فارسی
NEXORA سامانه‌ای وب‌محور برای یکپارچه‌سازی مدیریت اعضا، مربیان، باشگاه‌ها، اشتراک‌ها، پرداخت‌ها، برنامه‌های تمرینی و برنامه‌های تغذیه است. سامانه سه نقش اصلی دارد: مدیر باشگاه، مربی و ورزشکار.

### امکانات هدف
- ثبت‌نام و ورود کاربران و کنترل دسترسی مبتنی بر نقش
- مدیریت پروفایل ورزشکاران و مربیان
- مدیریت اطلاعات باشگاه و امکانات آن
- ساخت و مشاهده برنامه تمرینی شامل حرکت، ست، تکرار و وزنه
- ثبت و مشاهده برنامه تغذیه
- مدیریت اشتراک و وضعیت پرداخت
- ثبت سوابق تمرین و پرداخت
- گزارش‌های مدیریتی

### وضعیت فعلی
این مخزن در مرحله برنامه‌ریزی و مستندسازی است. موارد `TODO` و تصمیم‌های پیشنهادی باید با استاد و اعضای گروه تأیید شوند. وجود مستندات به معنی پیاده‌سازی‌شدن قابلیت‌ها نیست.

## English
NEXORA is a web-based system designed to centralize gym members, trainers, clubs, memberships, payments, workout plans, and nutrition plans. Its three primary roles are Gym Manager, Trainer, and Athlete.

### Planned features
- User registration, authentication, and role-based authorization
- Athlete and trainer profiles
- Gym information and facilities management
- Workout plans with exercises, sets, reps, and weights
- Nutrition plans
- Membership and payment status management
- Workout and payment history
- Management reports

### Current status
This repository is currently in the planning and documentation phase. Items marked `TODO` and proposed decisions must be confirmed by the instructor and team. Documentation does not mean that a feature has already been implemented.

## Repository structure
- `docs/` — bilingual project documentation
- `diagrams/` — editable PlantUML source files for UML and ERD
- `planning/` — backlog, milestones, and team responsibilities
- `src/` — application implementation area
- `tests/` — test strategy and future tests

## Proposed technology stack
- Python + Django
- HTML, CSS, Bootstrap, JavaScript
- SQLite during development; PostgreSQL if required for deployment
- Git and GitHub for version control

This is a proposal, not a confirmed instructor requirement.

## Team
- Amirabbas Ghadimi (امیرعباس قدیمی)
- Shayan Basharati (شایان بشارتی)
- Maedeh Mohammadi (مائده محمدی)

## How to start
1. Read `docs/01-vision.md`.
2. Confirm instructor requirements and scope.
3. Review `docs/02-requirements.md` and `planning/backlog.md`.
4. Confirm the technology stack before implementation.
5. Update this README as real implementation and testing progress.

## License
TODO: Choose a license only if the instructor/team requires one.
