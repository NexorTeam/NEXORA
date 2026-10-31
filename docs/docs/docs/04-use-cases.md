# موارد کاربرد | Use Cases

## UC-01: ورود به سامانه / Sign in
**Actor:** Any registered user  
**Precondition:** User account exists and is active.  
**Main flow:** User submits credentials → system validates them → system starts authenticated session → user is directed to the correct dashboard.  
**Alternative:** Invalid credentials produce a safe error message without revealing whether a username exists.  
**Postcondition:** Authenticated session exists.

## UC-02: ثبت ورزشکار / Register athlete
**Actor:** Gym Manager  
**Precondition:** Manager is authenticated and authorized.  
**Main flow:** Open member form → enter required fields → validate → save athlete profile and account association → show confirmation.  
**Exceptions:** Duplicate unique identifier or invalid fields are rejected.  
**Security:** Only authorized managers may create or edit member records.

## UC-03: ایجاد و تخصیص برنامه تمرینی / Create and assign workout plan
**Actor:** Trainer  
**Precondition:** Trainer is authenticated; target athlete exists and is within the trainer's allowed scope.  
**Main flow:** Create plan → add exercises → set sets/reps/optional weight and notes → select athlete → save and assign.  
**Exceptions:** Invalid values or missing required fields prevent saving.  
**Postcondition:** Assigned athlete can view the plan.

## UC-04: مدیریت اشتراک / Manage membership
**Actor:** Gym Manager  
**Main flow:** Select athlete → enter membership type and dates → set payment/status fields according to agreed rules → save → system displays current/expired status.  
**Business rule:** Date/status logic must be implemented consistently and covered by tests.

## UC-05: ثبت پرداخت / Record payment
**Actor:** Gym Manager  
**Main flow:** Select member/membership → enter amount, date, method, reference (optional), and status → validate → save record.  
**Security:** Only authorized staff can create or edit payment records; athletes can view only their own permitted history.

## UC-06: مشاهده اطلاعات شخصی / View personal information
**Actor:** Athlete  
**Main flow:** Sign in → open dashboard → view own profile, assigned plans, membership and payment history.  
**Security:** The server must enforce ownership checks, not just hide links in the UI.

## فارسی — نکته
این سناریوها پیش‌نویس‌اند. جزئیات فیلدها، قواعد پرداخت و حدود دسترسی باید با تصمیم نهایی گروه و دستور استاد هماهنگ شوند.
