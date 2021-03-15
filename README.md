# Module 9: Surfs_up

## Overview of Project
Using Python, SQlLite, & SQLAlchemy

### Purpose
A potential investor in your Surf Shop/Ice Cream store wants more information about temperature trends before opening the surf shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.  Deliverables include
* Determine the Summary Statistics for June
* Determine the Summary Statistics for December
* Submit a written report for the statistical analysis


## Results (Three Key Differences Between June and December)

![June_Temps](june_temp_stats.png) 
![December_Temps](december_temp_stats.png)

Based on the charts above.  We can see that:
* The minimum temperature can be significantly colder in December than in June (56 degrees versus 64 degrees) while the max temperatures are only 2 degrees off
* Nearly 200 more temperature counts were taken in December versus in June
* The average temperature are off by more than 3 degrees


## Summary: 
While temperatures in December can be lower than in June, the average, max, and quartiles are relatively similar.  This leads to the expectation of year round business for the Surf Shop/Ice Cream store

Two additional queries to perform to gather more weather data for June and December would be:
* june_precipitation = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()
* december_precipitation = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()

