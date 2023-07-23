# Household-Electric-Consumption-Over-Time-Analysis

# Introduction

This project dives into the study of global energy patterns and uses LSTM's in order try to predict global usage.

The source for the data can be found here: http://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption

# Data description: 

- date: Date in format dd/mm/yyyy
- time: time in format hh:mm:ss
- global_active_power: household global minute-averaged active power (in kilowatt)
    - The power that is actually used 
- global_reactive_power: household global minute-averaged reactive power (in kilowatt)
    - voltage / power that bouces back and forth between devices that is theoretically unused
- voltage: minute-averaged voltage (in volt)
- global_intensity: household global minute-averaged current intensity (in ampere)
    - ampere is abreviated with amp 
- sub_metering_1: energy sub-metering No. 1 (in watt-hour of active energy). It corresponds to the kitchen, containing mainly a dishwasher, an oven and a microwave (hot plates are not electric but gas powered).
- sub_metering_2: energy sub-metering No. 2 (in watt-hour of active energy). It corresponds to the laundry room, containing a washing-machine, a tumble-drier, a refrigerator and a light.
- sub_metering_3: energy sub-metering No. 3 (in watt-hour of active energy). It corresponds to an electric water-heater and an air-conditioner.

Data is measured in Paris, France in the date range December 2006 to November of 2010. 

# Initial analysis: 

Active and Reactive power: 

![](graphs/Screenshot%202023-07-20%20at%207.44.46%20PM.png)

- Weekly energy patterns and daily energy patterns are very similar in shape

- Similar observation in global reactive power 

![](graphs/Screenshot%202023-07-21%20at%203.13.05%20PM.png)

Voltage: 

![](graphs/Screenshot%202023-07-21%20at%203.20.08%20PM.png)

- Voltage is staying relatively constant, this can also be another important factor in determining patterns when we get to the model. 

Global intensity: 

![](graphs/Screenshot%202023-07-21%20at%203.24.26%20PM.png)

- There seems to be a pattern of peaks going on, further analysis will be required. 

Submetering: 

![](graphs/Screenshot%202023-07-21%20at%203.26.08%20PM.png)

- Sub meter three has the highest amount of energy usage.  
    - This makes sense as electric water heater and air conditioning are more likely to use more energy than kitchen appliances and washing appliances. 
- Sub meter three also seems to have some kind of patter in its peaks.

Seasonal patterns: 

- Months between 3 and 5 are considered Spring
- Months between 6 and 9 are considered Summer
- Months between 9 and 11 are considered Fall 
- Other = winter 

![](graphs/Screenshot%202023-07-22%20at%209.41.54%20PM.png)

- Highest average power consumption comes in the winter

![](graphs/Screenshot%202023-07-22%20at%209.43.59%20PM.png)

- Highest average reactive comes in the summer

![](graphs/Screenshot%202023-07-22%20at%209.45.14%20PM.png)

- highest all around meter per season is submeter 3 
- all meetrs peak in the winter, and have the lowest usage in the summer

- Overall it seems that winter is the highest active power time 
- Summer has the lowest active power and lowest metered power so it makes sense that it would have the highst amount of reactive power

Daily trends: 

![](graphs/Screenshot%202023-07-22%20at%209.48.03%20PM.png)

# Autocorrelation 

![](graphs/Screenshot%202023-07-22%20at%209.48.50%20PM.png)

- An autocorrelation score of 0.96 indicates that the current values of the time series are highly correlated with their past values. The time series tends to show a strong and persistent pattern that repeats over time.

# Cross correlation 

![](graphs/Screenshot%202023-07-22%20at%209.49.41%20PM.png)

- Global intensity is highly correlated with Global active power

- Heat map has the same result 

![](graphs/Screenshot%202023-07-22%20at%209.50.26%20PM.png)

