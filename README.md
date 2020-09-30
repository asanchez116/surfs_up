
# Surfs Up

## Overview of the statistical analysis:

A client as requested information about temperature trends before opening a shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if varying temperature might significantly affect the sustainability of the business year-round.



## Results:
1. The average temerature was 4 degrees warmer in June than December
2. The average temperature is 71.0 degrees for December months 
3. The average temperature is 74.9 degrees for June months 
4. The stdev was 3.25 in June vs 3.74 in December 
5. There are 183 fewer observations in December than June 



## Summary:

Temperatures were slghtly cooler in the December as would be expected but the variation is not large although December has a higher standard deviation indicating more spread 
183 fewer temperature measurements in December than June  
1. compare monthly trends of percipitation  
```sh
results = session.query(Measurement.prcp).filter(extract('month', Measurement.date)==12).all()
```
```sh
results = session.query(Measurement.prcp).filter(extract('month', Measurement.date)==12).all()
```
2. compare temperature trends for the previous year 
```
results = session.query(Measurement.tobs).filter(extract('year', Measurement.date)==2017).all()
```
```
results = session.query(Measurement.tobs).filter(extract('year', Measurement.date)==2016).all()
```