# Data Engineering test 

This is a test for data engineers at TakeOff Labs. 

## Submission 

* You have an hour to perform the following exercise
* **Please submit your answers in English 🇺🇸**
* Submit your results in a single zip (most convenient would be to use your preferred text editor and to write answers to the questions along with some comments) by email to the person responsible for your technical test

## Exercise

_Table_ : **Installs**

| Column Name  | Type        | Notes                   |
| ------------ | ----------- | ----------------------- |
| `id`         | `BIGINT`    |                         |
| `creator_id` | `BIGINT`    | `id` in Creators table  |
| `amount`     | `DOUBLE`    | US dollars              |
| `created_at` | `TIMESTAMP` |                         |
| `country`    | `TEXT`      | ISO Code                |
| `platform`   | `TEXT`      | in `{"iOS", "android"}` |

_Table_: **Creators**

| Column Name        | Type        | Notes                          |
| ------------------ | ----------- | ------------------------------ |
| `id`               | `BIGINT`    | `creator_id` in installs table |
| `created_at`       | `TIMESTAMP` |                                |
| `country`          | `TEXT`      | ISO Code                       |
| `last_signin_date` | `TIMESTAMP` |                                |

_Rk: in this exercise, consider that creators are responsible for generating installs_

**Using the schemas described above, write the following queries using whatever SQL, R, Python or whatever Programming language you'ld like:**

1. Daily Install Amounts. Resulting columns should be date and the total amount
2. Get the percent that the top 5 publishers contributed to overall earnings. Resulting column is simply one number (a percent)
3. Can you find the most inconsistent publisher ? We know that question is vague. We wish to find out who makes a lot of money but doesn't do so on a consistent basis so we can prioritize our outreach/account management. Please do describe your algorithm
4. How would you start diving into this data looking for fraud? What kind of signals would you look at? Try to draft tables / charts that would help us monitor fraud. 
