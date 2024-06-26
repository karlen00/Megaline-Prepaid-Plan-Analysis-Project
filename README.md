# README

## Megaline Prepaid Plan Analysis Project

### Project Description

You work as an analyst at a telecommunications operator company called Megaline. The company offers its clients two types of prepaid plans: the Surf plan and the Ultimate plan. The advertising department wants to know which prepaid plan generates more revenue so that they can allocate the advertising budget accordingly.

Your task is to analyze the behavior of clients and determine which prepaid plan brings in more revenue. This analysis is based on a sample of Megaline clients consisting of 500 user data entries, including information about who they are, where they come from, which plan they use, and the number of calls and messages they sent in 2018.

### Prepaid Plan Descriptions

#### Surf Plan
- Monthly fee: $20
- 500 minutes of calls per month
- 50 SMS per month
- 15 GB of data per month
- Charges after exceeding the plan limits:
  - 1 minute: 3 cents
  - 1 SMS: 3 cents
  - 1 GB of data: $10

#### Ultimate Plan
- Monthly fee: $70
- 3000 minutes of calls per month
- 1000 SMS per month
- 30 GB of data per month
- Charges after exceeding the plan limits:
  - 1 minute: 1 cent
  - 1 SMS: 1 cent
  - 1 GB of data: $7

### Instructions for Completing the Project

#### Step 1: Load the Data and Study General Information

The dataset used in this project consists of five files:
- `/datasets/megaline_calls.csv`
- `/datasets/megaline_internet.csv`
- `/datasets/megaline_messages.csv`
- `/datasets/megaline_plans.csv`
- `/datasets/megaline_users.csv`

#### Step 2: Prepare the Data

- Convert data to the necessary data types.
- Identify and eliminate errors in the data, such as calls with a duration of 0 minutes which may be missed calls.

For each user, calculate:
1. The number of calls made and minutes used per month.
2. The number of SMS sent per month.
3. The volume of data used per month.
4. The monthly revenue from each user (subtract the plan limits from the total number of calls, texts, and data; multiply the result by the per-unit rate; add the monthly fee based on the plan).

#### Step 3: Analyze the Data

- Describe consumer behavior.
- Determine the number of minutes, messages, and volume of mobile data used by users of each plan per month.
- Calculate the mean, variance, and standard deviation.
- Create histograms and describe the distribution.

#### Step 4: Test Hypotheses

1. The average revenue from Ultimate plan users and Surf plan users is different.
2. The average revenue from users in the NY-NJ area is different from users in other regions.

Explain how to formulate the null and alternative hypotheses. Determine the criteria for testing the hypotheses and the reasons for using them.

#### Step 5: Write a Comprehensive Conclusion

Format: Complete the task in Jupyter Notebook. Insert code into code cells and explanations into markdown cells. Format and title appropriately.

### Data Description

#### `users` table (user data):
- `user_id`: User ID
- `first_name`: User's first name
- `last_name`: User's last name
- `age`: User's age (years)
- `reg_date`: Registration date (dd-mm-yy)
- `churn_date`: Date the user stopped using the service (if blank or missing, the service is currently in use)
- `city`: User's city of residence
- `plan`: Name of the phone plan

#### `calls` table (call data):
- `id`: Unique call ID
- `call_date`: Call date
- `duration`: Call duration (in minutes)
- `user_id`: User ID who made the call

#### `messages` table (SMS data):
- `id`: Unique SMS ID
- `message_date`: Date SMS was sent
- `user_id`: User ID who sent the SMS

#### `internet` table (web session data):
- `id`: Unique web session ID
- `mb_used`: Data volume used during the session (in megabytes)
- `session_date`: Web session date
- `user_id`: User ID

#### `plans` table (phone plan data):
- `plan_name`: Name of the phone plan
- `usd_monthly_fee`: Monthly fee in USD
- `minutes_included`: Monthly call minute allowance
- `messages_included`: Monthly SMS allowance
- `mb_per_month_included`: Monthly data allowance (in megabytes)
- `usd_per_minute`: Price per minute after exceeding the plan allowance
- `usd_per_message`: Price per SMS after exceeding the plan allowance
- `usd_per_gb`: Price per additional gigabyte of data after exceeding the plan allowance (1 GB = 1024 megabytes)

### Conclusion

This document provides an overview of the Megaline prepaid plan analysis project. All analyses are conducted in Jupyter Notebook using Python programming language and data analytics libraries such as Pandas, NumPy, and Matplotlib. The results of this analysis will help the advertising department design more effective marketing strategies based on the most profitable plan.
