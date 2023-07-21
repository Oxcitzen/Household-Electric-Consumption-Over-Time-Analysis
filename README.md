# Household-Electric-Consumption-Over-Time-Analysis

# Introduction

This project dives into the study of global energy patterns and uses LSTM's in order try to predict global usage.

The source for the data can be found here: http://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption

Data description: 

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


