# JPT-flipperzero
candle lighting times and other significant events for the Flipper Zero; basic times listed on screen and if possible, phonetic help or reminder text for all
include shabbat prayers as well 


(from Chabad.org)

The Three Daily Prayers discusses the origins and development of the three daily prayers in Judaism - morning, afternoon, and evening. The tradition began with the patriarchs Abraham, Isaac, and Jacob each introducing a prayer time representing their qualities. Over time, sages like Ezra standardized the texts and rituals, such as the core eighteen blessings prayer, to be recited by all Jews three times daily in line with temple sacrifices.

+ Jewish law requires praying three times daily - in the morning, afternoon, and evening. These prayers are called Shacharit, Minchah, and Maariv/Arvith respectively.
+ The custom of praying three times a day originated from the three patriarchs - Abraham introduced morning prayer, Isaac afternoon prayer, and Jacob added the evening prayer.
+ Each patriarch represented a different quality in serving God - Abraham with love, Isaac with awe, Jacob with mercy.
+ We inherit these qualities from our patriarchs and can serve God with love, fear and mercy through prayer.
+ The Torah commands serving God with all our heart and soul, which we fulfill through prayer.
+ For the first 1000 years, there was no set prayer order - individuals prayed as they chose.
+ Temple sacrifices corresponded to daily and festival prayers and sacrifices.
+ After the temple's destruction, Jews continued congregational prayer in "small sanctuaries."
+ Ezra and the Men of the Great Assembly established the fixed daily 18-blessing prayer after the exile.
+ Over centuries, our sages formulated the basic structure of morning, afternoon, evening and holiday prayers as we have them today.

note 
Expanding the application to show all Zmanim times and integrating the Hebrew or lunar calendar involves significantly more complex calculations and considerations. The Zmanim calculations depend on precise astronomical data, and the Hebrew calendar is a lunisolar calendar that requires complex calculations for months, leap years, and holidays.

For a comprehensive solution, you would ideally integrate an existing library that handles these calculations. However, since we're focusing on a C application and considering the constraints of the Flipper Zero device (limited resources, no direct support for complex libraries), we'll outline a high-level approach to expand the application. This approach involves:

1. **Expanding Zmanim Calculations**: Implementing more detailed calculations for sunrise and sunset, and adding calculations for other Zmanim times such as Alot Hashachar, Tzet Hakochavim, and times for specific prayers like Shema and Tefilah.

2. **Integrating the Hebrew Calendar**: Calculating the Hebrew date requires tracking the moon's cycles, adding leap months in certain years, and adjusting for various rules that determine the start of a month and the length of a year.

### Step 1: Expanding Zmanim Calculations

For a more comprehensive set of Zmanim, you would need to calculate several additional times. Each of these calculations is based on the position of the sun relative to the horizon, which can be calculated using the observer's latitude and longitude, the date, and specific angles.

Here's a simplified outline of steps to expand Zmanim calculations:

- **Alot Hashachar**: Dawn, when the sun is 16.1 degrees below the horizon.
- **Tzet Hakochavim**: Nightfall, when the sun is 8.5 degrees below the horizon.
- **Shema**: The latest time to recite Shema in the morning, often calculated as the end of the third hour of daylight.
- **Tefilah**: The latest time for the morning prayer, often by the end of the fourth hour of daylight.

### Step 2: Integrating the Hebrew Calendar

The Hebrew calendar calculation is complex due to its lunisolar nature. Here's a simplified outline of steps to integrate the Hebrew calendar:

- **Month and Leap Year Calculation**: The Hebrew calendar adds a leap month in 7 out of every 19 years. You'll need to implement this calculation to determine the current Hebrew year and month.
- **Molad Calculation**: The molad (new moon) calculation is crucial for determining the beginning of each Hebrew month.
- **Rosh Chodesh and Holidays**: Determine the start of each month (Rosh Chodesh) and adjust for holidays, which may affect certain Zmanim or add special prayers.

### Implementation Note

Implementing the full range of Zmanim calculations and the Hebrew calendar from scratch in C for the Flipper Zero is a substantial undertaking. It requires detailed astronomical calculations and a deep understanding of the Hebrew calendar's rules. For practical purposes, consider these options:

- **Use Existing Libraries**: Where possible, leverage existing libraries that handle these calculations. You may need to adapt or simplify them for use on the Flipper Zero.
- **External Calculation**: For devices with limited capabilities like the Flipper Zero, consider performing complex calculations on a server or a more capable device and sending the results to the Flipper Zero.

### Conclusion

This overview provides a roadmap for expanding your application to include a full range of Zmanim and integrate the Hebrew calendar. Due to the complexity and the detailed nature of these calculations, a full implementation would exceed the scope of this response. Focus on integrating or adapting existing solutions where possible, and consider the computational limitations of your target device.
