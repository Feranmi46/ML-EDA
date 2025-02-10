Overview
-----------
This dataset provides insights into the dating app usage patterns and preferences of Generation Z (individuals aged 18-25) in India. It includes demographic information, app usage habits, user preferences, and satisfaction levels. The dataset is valuable for researchers, marketers, and dating app developers who want to understand the evolving landscape of online dating among young adults.

Data Dictionary
-----------------
|Column Name      |     Data Type      |     Descriptin |
|-----------------|--------------------|----------------|
|Age              |       Integer      |Age of the user (18-25 years).|
|Gender           |       String       |User's self-identified gender (male, female, non-binary, other).|
|Location         |      String        |City or region where the user resides.|
|Education        |     String         |User's highest level of education.|
|Occupation       |     String         |User's employment status or job role.|
|Primary_App      |     String         |The main dating app used by the user.|
|Secondary_Apps   |    String          |Other dating apps used by the user.|
|Usage_Frequency  |     String         |How often the user uses dating apps (e.g., daily, weekly, monthly).|
|Reason_for_Using |      String        |The user's motivation for using dating apps (e.g., casual dating, finding a serious relationship, social interaction).|
|Satisfaction     |   Integer          |User's satisfaction level on a scale of 1 (very dissatisfied) to 5 (very satisfied).|
|Challenges       |String              |Issues faced while using dating apps (e.g., safety concerns, lack of genuine matches).|
|Desired_Features |String              |Features users wish to see in dating apps (e.g., video/audio calls, detailed profiles).|
|Preferred_Communication |String       |The preferred way users communicate on dating apps (e.g., texting, video calls).|
|Daily_Usage_Time | Float              |Estimated time spent on dating apps per day (in hours).|


Data Cleaning Steps
----------------------------------
The following cleaning steps were applied to ensure the dataset is accurate and usable:
1) Standardized Categorical Values
    * Converted all categorical text columns to lowercase.
    * Ensured consistent formatting (e.g., Male and male were unified).
    
2) Handled Missing Values
    * Identified missing values using df.isnull().sum().
    * Categorical Columns: Filled missing values with 'None' 

3) Removed Outliers
    * Used the Interquartile Range (IQR) method to detect and remove outliers in "Age" and "Satisfaction."
    * No significant outliers were found in "Age" (expected range: 18-25).
    * Satisfaction scores outside the 1-5 range were corrected.

4) Ensured Correct Data Types
    * Converted all neccesary columns to category format.
  

How to Use This Dataset
---------------------------------
This dataset can be used for:
1) Market Research: Understanding dating trends among Gen Z in India.
2) Feature Development: Improving dating app features based on user preferences.
3) Behavioral Analysis: Exploring how demographics influence online dating habits.
4) Data Science & AI Models: Training recommendation systems for matchmaking.


Key Insights
------------------------
1) Younger Gen-Z (18-22) are the most active users, but engagement drops as they age.
2) Tinder is dominant among younger users, while Hinge and OkCupid gain popularity among older Gen-Z.
3) Metro city users use a wider variety of apps compared to those in smaller towns.
4) Safety concerns and time-wasting are the most common challenges faced by users.


Data Processing
--------------------
1) Categorical Encoding: Applied One-Hot Encoding for non-ordinal variables (Gender, Location, Apps, etc.).
2) Numerical Normalization: Used MinMaxScaler to scale Age, Daily Usage Time, and Satisfaction.
3) Feature Engineering: Created a new feature, Active App Count, to measure app diversity per user.

----------------------------------------
----------------------------------------
Author: Oluwaferanmi Osunbajo
