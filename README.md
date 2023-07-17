# scrape_mars
##Part 1: Scrape Titles and Preview Text from Mars News
Open the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. You will work in this code as you follow the steps below to scrape the Mars News website.

1. Use automated browsing to visit the Mars news siteLinks to an external site.. Inspect the page to identify which elements to scrape.

2. Create a Beautiful Soup object and use it to extract text elements from the website.

3. Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:

    * Store each title-and-preview pair in a Python dictionary and, give each dictionary     two keys: title and preview. An example is the following:

    * Store all the dictionaries in a Python list.

    * Print the list in your notebook.

    4. Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file. (Note: there will be no extra points for completing this.)


##List of titles and Previews


    [{'Title: Curiosity Mars Rover Reaches Long-Awaited Salty Region': 'Preview: The latest findings provide greater detail on a region of the Red Planet that has a watery past and is yielding promising samples for the NASA-ESA Mars Sample Return campaign.',
  "Title: NASA's InSight Waits Out Dust Storm": 'Preview: Despite signs of wear, the intrepid spacecraft is about to start an exciting new chapter of its mission as it climbs a Martian mountain.',
  "Title: 10 Years Since Landing, NASA's Curiosity Mars Rover Still Has Drive": 'Preview: InSightâ\x80\x99s team is taking steps to help the solar-powered lander continue operating for as long as possible.',
  'Title: NASA To Host Briefing on InSight, Mars Reconnaissance Orbiter Findings': 'Preview: After years of climbing, the Mars rover has arrived at a special region believed to have formed as Marsâ\x80\x99 climate was drying.',
  "Title: NASA's InSight 'Hears' Its First Meteoroid Impacts on Mars": 'Preview: â\x80\x9cSelfieâ\x80\x9d of the Curiosity rover with inset showing the SAM instrument prior to installation on the rover.',
  'Title: NASA and ESA Agree on Next Steps to Return Mars Samples to Earth': 'Preview: The Mars landerâ\x80\x99s seismometer has picked up vibrations from four separate impacts in the past two years.',
  "Title: NASA Prepares to Say 'Farewell' to InSight Spacecraft": 'Preview: Protecting Mars Sample Return spacecraft from micrometeorites requires high-caliber work.',
  "Title: NASA's InSight Lander Detects Stunning Meteoroid Impact on Mars": 'Preview: A closer look at what goes into wrapping up the mission as the spacecraftâ\x80\x99s power supply continues to dwindle.',
  'Title: NASA to Host Briefing on Perseverance Mars Rover Mission Operations': 'Preview: For the first time in its eight years orbiting Mars, NASAâ\x80\x99s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27.',
  'Title: Why NASA Is Trying To Crash Land on Mars': 'Preview: Scientists from two Mars missions will discuss how they combined images and data for a major finding on the Red Planet.',
  'Title: Mars Mission Shields Up for Tests': 'Preview: The agencyâ\x80\x99s Perseverance rover will establish the first sample depot on Mars.',
  "Title: NASA's Perseverance Makes New Discoveries in Mars' Jezero Crater": 'Preview: The agencyâ\x80\x99s lander felt the ground shake during the impact while cameras aboard the Mars Reconnaissance Orbiter spotted the yawning new crater from space.',
  "Title: SAM's Top 5 Discoveries Aboard NASA's Curiosity Rover at Mars": 'Preview: Members of the mission will discuss the roverâ\x80\x99s activities as it gathers samples in an ancient river delta.',
  "Title: NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm": 'Preview: Like a carâ\x80\x99s crumple zone, the experimental SHIELD lander is designed to absorb a hard impact.',
  "Title: NASA's Perseverance Rover Investigates Geologically Rich Mars Terrain": 'Preview: The rover found that Jezero Craterâ\x80\x99s floor is made up of volcanic rocks that have interacted with water.'}]

## Analyze the Data


Analyze your dataset by using Pandas functions to answer the following questions:
1. How many months exist on Mars?  

	A:  We do not indicate the number of months on Mars in our dataset.  From our knowledge of finishing this data analysis, there are approximately 687 earth days in a Mars year.  If we took the idea of a month being equal to 28 days, we would determine that there are 24 and a half earth months on Mars.  This information was confirmed by the Mars Calendar at interimm.org.  
	
	As can be seen on the Royal Museum of Greenwich's website, a day on Mars is 40 minutes longer than that of a day on earth.  This is based on the Solar day (sol).  This is the time it takes to rotate on an axis and come back the same position in the day.  Therefore, it would be safe to say that Mars has 24 months in each calendar year.  For the purposes of this analysis, the calendar years used were that of the earths.  If the day are the same on Earth and on Mars, why does the Earth have less days in its calendar year than Mars?  Calendar years are based on one revolution around the sun.  Mars is further away from sun and it's trip takes approximately twice as long as the Earth.  
	
	References:
	https://www.rmg.co.uk/stories/topics/how-long-day-on-mars#:~:text=year%20on%20Mars%3F-,Mars%20is%20a%20planet%20with%20a%20very%20similar%20daily%20cycle,than%20a%20day%20on%20Earth.
	
	https://interimm.org/mars-clock/en/cal-doc.html#:~:text=In%20general%2C%20there%20are%2024,or%20Spring%20Equinox%20on%20Mars.
	
2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?
	
	A:  The number of Martian and Earth days are equivalent as can be seen in the mars_df dataframe.  Therefore, there are 1867 Mars days.  Also, from the first question, we know that a day on Mars 
	
3. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:

<div align="center"> 

Minimum Temperature(°C) for each "Month" on mars (based on Terrestrial Months)
	
![](https://github.com/TraceyGeneau/scrape_mars/blob/main/Starter_Code/output/cold_month_on_mars.png)	

</div>

 
 A: From the average minimum temperature, it was determined that the temperature was the coldest month was the third at -83.3°C with the fourth month being the second coldest at -82.7°C.  The warmest month on Mars was the 8th month at -68.4°C.  Although we generally have a lot warmer temperatures on Earth, the Coldest temperautre recorded on earth was -89.2°C.  Fortunately, these tempeartures are isolated to places such as the Antartica.

Reference
https://wmo.asu.edu/content/world-lowest-temperature
	
4. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:

<div align="center"> 

Atmospheric Pressure mm(Hgg) for each "Month" on mars (based on Terrestrial Months)
	
![](https://github.com/TraceyGeneau/scrape_mars/blob/main/Starter_Code/output/avg_pressure_on_mars.png)	

</div>

A:  The month is the highest atmospheric pressure was the 9th month with 913.3 mmHg whereas the lowest was the 6th month with 745.1 mmHg.  


5. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:

<div align="center"> 

Solar Days (Sol) as compared to the Mininmum Temperature (°C) on Mars
	
![](https://github.com/TraceyGeneau/scrape_mars/blob/main/Starter_Code/output/mintempvsterrdays.png)	

</div>

<div align="center"> 

Data Frame of the Solar Days and Minimum Temperature (°C)
	
![](https://github.com/TraceyGeneau/scrape_mars/blob/main/Starter_Code/output/terre_df.png)	

</div>



	A:  We can see in the graph above that at approximately 500 days we get a lowest peak or winter peak.  From the terr_sort_df we can get an approximate sol = 535.  The next peak occurs about 1200-1250.  From this we get a sol from 1219 to 1237.  The mid point is 1224.  The difference between these two points is 689.  From the NASA "Mars: The Red Planet" website, it was confirmed that a Mars year is equivalent to 687 earth days. 

	Reference
	(ttps://solarsystem.nasa.gov/planets/mars/in-depth/#:~:text=Rotation-,Orbit%20and%20Rotation,same%20as%20687%20Earth%20days.)


