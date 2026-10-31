# مدل داده | Data Model (Draft)

## Proposed entities
- **User:** authentication identity, username/email, password hash managed by Django, active status
- **Role/Profile:** role assignment and role-specific profile data
- **Gym:** name, address, description, facilities
- **TrainerProfile:** user reference, specialties, credentials, biography
- **AthleteProfile:** user reference, basic profile fields, goals (only if necessary)
- **Exercise:** name, description, target muscle/group, media path/URL (optional), safety notes
- **WorkoutPlan:** title, trainer, athlete, start/end dates, notes, status
- **WorkoutPlanItem:** workout plan, exercise, ordering, sets, reps, optional weight, rest duration
- **NutritionPlan:** title, trainer, athlete, start/end dates, general notes
- **Membership:** athlete, gym, plan/type, start date, end date, status
- **Payment:** membership, amount, date, method, status, optional reference
- **WorkoutLog:** athlete, plan item/exercise, date, performed sets/reps/weight, notes (scope to confirm)

## Relationships
- A user has one appropriate role/profile for the first version.
- A trainer can create multiple workout plans.
- A workout plan belongs to one assigned athlete and contains one or more plan items.
- Each plan item references one exercise.
- An athlete can have multiple membership records over time.
- A membership can have multiple payment records if installments are supported.
- An athlete can have multiple nutrition plans and workout logs.

## Design questions to resolve
- Can one account hold more than one role?
- Can a trainer work at multiple gyms?
- Does a membership belong to one gym only?
- Are partial payments/refunds required?
- Does workout history track each set or only session completion?
- Which personal data is genuinely needed for the course project?

## Data protection
Collect only necessary personal data. Use fictional sample records. Do not store medical diagnoses or sensitive health data unless explicitly required and appropriately handled.
