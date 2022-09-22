# (Ford Bike Exploration)
## by (Abid Mohamed Nadhir)


## Dataset

> My chosen DataSet is showing information that covers over 180K records of individual rides made in a bike-sharing system covering the greater San Francisco Bay area in Feb-2019.
  RangeIndex: 183412 entries, 0 to 183411
  Data columns (total 16 columns):
index   Column                   Non-Null Count   Dtype  
---  ------                   --------------   -----  
 0   duration_sec             183412 non-null  int64  
 1   start_time               183412 non-null  object 
 2   end_time                 183412 non-null  object 
 3   start_station_id         183215 non-null  float64
 4   start_station_name       183215 non-null  object 
 5   start_station_latitude   183412 non-null  float64
 6   start_station_longitude  183412 non-null  float64
 7   end_station_id           183215 non-null  float64
 8   end_station_name         183215 non-null  object 
 9   end_station_latitude     183412 non-null  float64
 10  end_station_longitude    183412 non-null  float64
 11  bike_id                  183412 non-null  int64  
 12  user_type                183412 non-null  object 
 13  member_birth_year        175147 non-null  float64
 14  member_gender            175147 non-null  object 
 15  bike_share_for_all_trip  183412 non-null  object 
dtypes: float64(7), int64(2), object(7)

> Data Wrangling 
  * we did some data assessing and cleaning to treat the following problems:
   * start_time and end_time columns in object dtype
   * start_station_id and end_station_id columns in int64 dtype
   * start_station_latitude, start_station_longitude, end_station_latitude, and end_station_longitude columns in float64 dtype
   * bike_id column in int64 dtype
   * user_type in object dtype
   * Adding Age column
   * drop NaN values
   * delete all ages Above 90 take into consideration the date of the data (2019)
   * Add day, week_day, hour, day_part columns from the start_time and end_time columns
   * Drop Gender Outliers "Other" since it represents less than 2%

## Summary of Findings

> * There is multiple observations such the type of user and duration were customer riding duration tend to be more than subscribers
    The weekend days duration of riding is way more than other days
    People who are at age 20 to around 50 ride duration is high and people from 20 to 30 are the highest

> * The distrubution of the data is clearly good we don't have outliers the only variable with a skewed histograme is the duration and we didn't preform any transformation since it is clearly skewed.
 
  * For male customers most riding duration when the customer starts the ride in the second week of the month
  * For male customers most rides duration ends with the 10th of the month
  * For Female customers the rides with the most duration are in the second week of the month too
  * For Female customers rides ends between the 10th and the 15th are with the most duration
  * Subscribers both male and female don't give that much of details
  * Male customers rides with the most duration Starts before 5 and ends around 5
  * Female customers rides with the msot duration starts also before 5 but ends also bfore 5
  * Females who starts thier rides before 5 and those who ends thier rides before 5 tend to ride more than male in all times
  * Most duration rides by female subscribers ends before 5
  * Male and females most duration rides are in the Weekend
  * in All week days female riding duration is bigger than male riding duration
  * Subscribers riding is stable in all the week
  * Customers riding duration peak is in the weekend
  * Customers riding duration are higher than subscribers in the whole week

> * The type of user and the gender has an influence on the use of this service.

    Duration of use:
        Subscribers tends to have stable duration usage than Customers
        Subscribers duration usage is way less than Customers
        Subscribers usage is more than Customers
        Female rides duration are more than male durations

    Days of use
        Subscribers tends to use the service in weekdays, in contrast Customers focusses more on weekends
        the first two weeks of the month are with the most rides durations

    Hours of use
        Customers Male and Females peak duration rides before 5.
        Customers Male and Females peak duration rides ends before 5.
        Male customers duration riding is low and stable and opposite for female customers



## Key Insights for Presentation
> * Does gender affect the duration of the ride in the weekdays ?

> * What is the relation between user type and ride duration and days ? 

> * How time, gender and user type are related ?




