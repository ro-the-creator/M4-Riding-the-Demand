## Cleaning/EDA READ ME:

<p align='center'>
There is general information within this file, mainly pertaining to the dataset. There are also some generalized answers to key questions posed during the analysis. These were answered during the exploration, whereas the main README file has polished answers.

</p>

### Dictionary:

	- instant: record index

	- dteday : date

	- season : season (1:springer, 2:summer, 3:fall, 4:winter)

	- yr : year (0: 2011, 1:2012)

	- mnth : month ( 1 to 12)

	- hr : hour (0 to 23)

	- holiday : whether day is holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)

	- weekday : day of the week

	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
    
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog

	- temp : Normalized temperature in Celsius. The values are divided to 41 (max)

	- atemp: Normalized feeling temperature in Celsius. The values are divided to 50 (max)

	- hum: Normalized humidity. The values are divided to 100 (max)

	- windspeed: Normalized wind speed. The values are divided to 67 (max)

	- casual: count of casual users

	- registered: count of registered users

	- cnt: count of total rental bikes including both casual and registered

> [!INFO]
> Capital bikeshare has two types of passes available for the riders: Casual (Single-Trip, 24 Hour Pass or 3 Day Pass) and Registered (Monthly or Annual Membership)

<br>

### Stakeholder Demands

1) **Product Manager (PM)**: Demand, hotspots over time, holidays

2) **Operations Lead**: Times when bikes are used the least --> Best maintenance times, staffing for higher days

3) **Marketing Lead**: When/Who/How to launch promotions

4) **Policy & Ethics Director**: Honestly just making sure that we do everything above ethically and with inclusion/transparency in mind.

<br>

### Therefore... let's answer these questions:

- What are the busiest seasons? months? days? hours?
- what do holidays look like for bike usage?

<br>

- What days/hours are bikes used the most, for more staffing?
- What days/hours are bikes used the least for mainenance?

<br>

- Which holidays are least users using to target promotions?

<br>

### At a Glance Answers:

1. **Fall** is the busiest season, **August** is the busiest month, **Friday** is the busiest day, and **evening hours** are the busiest times.
    - **Spring** is the driest season, **January** is the driest month, **Sunday** is the driest day, and **early morning** hours (between 3-4am) are the driest times.

<br>

2. Since bikes are typically only replaced when deemed necessary, I looked more into the days of the week and times of day that would be suitable for maintenance.
    - Typically, **Thurs/Fri/Sat** are the most used days, with the most used hours remaining consistent with the overall most used hours.
    - The least used days are **Sun/Mon/Tues**, with the times also remaining consistent with the overall least busy hours.
    - The *least busiest* hours are: **4am, 3am, 2am**. The *busiest* hours are **5pm, 6pm, 8am**.

<br>

3. The holidays show something else that's interesting. **April** is the highest registered users use, and **November** follows closely behind.  **December** is the least used month.
    - There may be potential to boost sales through promotions in July and September, particularly with promotions during 4th of July or Labor Day.
