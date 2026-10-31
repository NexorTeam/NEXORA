# داستان‌های کاربر | User Stories

## فارسی
### مدیر باشگاه
- به‌عنوان مدیر، می‌خواهم ورزشکار جدید ثبت کنم تا اطلاعات اعضا متمرکز باشد.
- به‌عنوان مدیر، می‌خواهم مربی و تخصص‌های او را ثبت کنم تا اعضا اطلاعات معتبر داشته باشند.
- به‌عنوان مدیر، می‌خواهم اشتراک‌ها و تاریخ انقضا را پیگیری کنم تا عضویت‌های منقضی مشخص شوند.
- به‌عنوان مدیر، می‌خواهم پرداخت‌ها را ثبت و گزارش بگیرم تا وضعیت مالی قابل پیگیری باشد.
- به‌عنوان مدیر، می‌خواهم گزارش اعضا و اشتراک‌ها را ببینم تا تصمیم‌گیری ساده‌تر شود.

### مربی
- به‌عنوان مربی، می‌خواهم پروفایل و تخصصم را مدیریت کنم.
- به‌عنوان مربی، می‌خواهم برنامه تمرینی با حرکت، ست، تکرار و وزنه بسازم.
- به‌عنوان مربی، می‌خواهم برنامه را به ورزشکار مشخصی تخصیص دهم.
- به‌عنوان مربی، می‌خواهم برنامه تغذیه و سوابق مجاز ورزشکار را بررسی کنم.

### ورزشکار
- به‌عنوان ورزشکار، می‌خواهم وارد حسابم شوم و اطلاعات شخصی‌ام را ببینم.
- به‌عنوان ورزشکار، می‌خواهم برنامه تمرینی و تغذیه تخصیص‌یافته را ببینم.
- به‌عنوان ورزشکار، می‌خواهم وضعیت و تاریخ انقضای اشتراکم را مشاهده کنم.
- به‌عنوان ورزشکار، می‌خواهم سوابق تمرین و پرداخت خودم را مشاهده کنم.

## English
- As a manager, I want to register athletes so member data is centralized.
- As a manager, I want to maintain trainer profiles and specialties.
- As a manager, I want to track membership dates and expiry.
- As a manager, I want to record payments and review financial summaries.
- As a trainer, I want to create workout plans with exercises, sets, reps, and optional weight.
- As a trainer, I want to assign plans to specific athletes.
- As a trainer, I want to maintain nutrition plans and review authorized progress.
- As an athlete, I want to view my profile, assigned plans, membership status, and personal history.

## Acceptance criteria examples
1. A non-manager cannot open manager-only member administration pages.
2. An athlete cannot view another athlete's private plan by changing an ID in the URL.
3. A workout plan cannot be saved without a title and at least one valid exercise item.
4. A membership end date cannot be earlier than its start date.
5. A payment amount cannot be negative.
