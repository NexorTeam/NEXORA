# نیازمندی‌ها | Software Requirements Specification (Draft)

**Version:** 0.1 — Draft / پیش‌نویس

## 1. نقش‌ها | Roles
- **مدیر باشگاه / Gym Manager**
- **مربی / Trainer**
- **ورزشکار / Athlete**

یک کاربر نباید صرفاً با تغییر رابط کاربری به داده‌های نقش دیگر دسترسی پیدا کند؛ مجوزها باید در سمت سرور بررسی شوند.

## 2. نیازمندی‌های کارکردی | Functional requirements

| ID | Requirement / نیازمندی | Priority |
|---|---|---|
| FR-01 | ثبت‌نام، ورود، خروج و تغییر رمز عبور / Registration, login, logout, password change | Must |
| FR-02 | کنترل دسترسی مبتنی بر نقش / Role-based access control | Must |
| FR-03 | مدیر بتواند اطلاعات ورزشکاران را ایجاد، مشاهده، ویرایش و غیرفعال کند / Manager manages athlete records | Must |
| FR-04 | ثبت پروفایل مربی، تخصص و مدارک / Trainer profile, specialties, credentials | Should |
| FR-05 | ثبت اطلاعات باشگاه، آدرس و امکانات / Gym details, address, facilities | Should |
| FR-06 | مدیریت کتابخانه حرکات با نام، توضیح و رسانه آموزشی اختیاری / Exercise library | Should |
| FR-07 | ایجاد برنامه تمرینی و تعیین حرکت، ست، تکرار و وزنه / Workout plan creation | Must |
| FR-08 | تخصیص برنامه به ورزشکار / Assign plans to athletes | Must |
| FR-09 | ثبت و مشاهده برنامه تغذیه / Nutrition plan management | Should |
| FR-10 | ایجاد اشتراک با تاریخ شروع، انقضا و وضعیت / Membership lifecycle | Must |
| FR-11 | ثبت پرداخت با مبلغ، تاریخ، روش و وضعیت / Payment records | Must |
| FR-12 | مشاهده سوابق تمرین و پرداخت شخصی / Personal histories | Should |
| FR-13 | گزارش پایه از اعضا، اشتراک‌های منقضی و پرداخت‌ها / Basic reports | Should |
| FR-14 | اعتبارسنجی فرم‌ها و نمایش پیام خطا / Form validation and feedback | Must |
| FR-15 | جست‌وجو و فیلتر اعضا و اشتراک‌ها / Search and filtering | Could |

Priorities: Must = required for first demonstrable version; Should = important if time allows; Could = optional.

## 3. نیازمندی‌های غیرکارکردی | Non-functional requirements
- **NFR-01 Security:** store passwords using the framework's secure password hashing; never store plain-text passwords.
- **NFR-02 Authorization:** check permissions on the server for every protected operation.
- **NFR-03 Privacy:** athletes can access only their own private profile, plans, and records unless explicitly authorized.
- **NFR-04 Usability:** forms and navigation should be understandable in Persian; interface should support right-to-left layout where appropriate.
- **NFR-05 Maintainability:** separate models, views, templates, and tests; use readable names and document setup.
- **NFR-06 Reliability:** invalid input should not create partial or inconsistent records.
- **NFR-07 Portability:** provide reproducible setup instructions for a standard development laptop.
- **NFR-08 Localization:** provide Persian and English documentation; interface language support depends on agreed scope.
- **NFR-09 Testing:** core access, membership, payment, and plan workflows must have automated or documented tests.
- **NFR-10 Data safety:** use fictional demo data; do not commit private or real user data.

## 4. قواعد کسب‌وکار | Business rules
- A membership has a start date, end date, and status.
- A payment record must have a non-negative amount, date, method, and status.
- A trainer may edit only plans they own or are authorized to manage.
- An athlete may view only plans assigned to them and their own private records.
- A workout-plan item references an exercise and stores sets/reps; weight can be optional depending on the exercise.
- Membership status should be derived or validated consistently against dates and payment state; the team must choose and document the exact rule.
- Nutrition plans are informational and do not replace professional medical advice.

## 5. Open questions / موارد نیازمند تأیید
- Instructor-required language/framework and deliverables
- Whether the app is single-gym or multi-gym
- Whether self-registration is allowed or managers create all accounts
- Whether payments are manual records or online payments
- Whether Persian/English applies to the interface or documentation only
- Required diagrams, report format, and grading rubric
