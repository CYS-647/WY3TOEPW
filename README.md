# WY3TOEPW
This script is to convert historical weather files stored in WY3 format into EPW format so it could be used for Building Energy Simulation. 

## Brief Background on weather data used in Building Energy Simulation
Building Energy Simulation(BES) is a common practice used to compare and evaluate the relative energy performance of different building designs. To reduce overall energy usage and carbon emissions, many jurisdictions now require the submission of building energy models to ensure new buildings are designed with better energy efficiency than corresponding basline designs - which are modelled based on older building standards with less stringent efficiency requirements. 

One of the essential inputs for BES is weather data. Weather data describes the expected external conditions a proposed building will experience based on its location. The current accepted practice is to use Typical Year weather files(such as TMY- Typical Meteorological Year in the US or CWEC - Canadian Weather Year for Energy Calculation in Canada) to run BES. 

For those who are unfamiliar, Typical Year weather files are created based on statistical methods, the objective is to select 12 representatitve months(each month in a calendar year is represented by a representative month) from 15 to 30 years of historical weather data. While the use of Typical Year weather data in BES generally saves computation time, the weather data itself often lacks representation of more extreme weather conditions, which could be useful for in depth building simulations. Since the status quo for running BES is to use Typical Year weather files, access to historical weather data in formats ready for simulation is often limited. 

In Canada, we are fortunate to have access to both Typical Year weather files and historical weather data through Environment and Climate Change Canada. However, the historical weather data is only available in wy3 format, which most software used for BES is unable to read directly. There is a need for a conversion tool. 

## Origins of the weather converter project
Previously, I worked on a paper detailing a method to convert historical weather data stored in wy3 format into simulation ready weather files in epw format (a link is included below for those who are interested to learn more). To demonstrate the method in practice, a script written using the MATLAB syntax is submitted with the paper. While MATLAB is a common language used by the research community, licenses are relatively expensive for average users. In the spirit of making the converter more accessible to average users, I decided to write a new script in Python - a popular open source language.  

## How to use this tool
1. Download the script and place it in the desired folder

2. Download weather data from the Environment and Climate Change Canada website. Place files in the appropriate folders - Make sure historical weather data and Typical Year weather files are stored separately

3. Check open the script, check and change relative paths accordingly 

4. Run the script 
* a. Load required libraries 
* b. Load functions located at the bottom of the jupyter notebook
* c. Run either Option 1 or Option 2 of script
    * Option 1 - Single location: reads in historical and typical weather data to produce epw weather files for each year
    * Option 2 - Batch Process : reads in files stored in designated folders, matches historical and typical weather data based on weather station number, batch           process the mathced weather data and produces epw weather files for each year at each location. 
      
  

## Relevant links
Weather Datasets published - by Environment and Climate Change Canada
https://climate.weather.gc.ca/prods_servs/engineering_e.html

EnergyPlus Weather File (EPW) Data Dictionary - Big Ladder Software
https://bigladdersoftware.com/epx/docs/8-3/auxiliary-programs/energyplus-weather-file-epw-data-dictionary.html

Calculation of Relative Humidity by Australian Government - Bureau of Meteorology
http://www.bom.gov.au/climate/averages/climatology/relhum/calc-rh.pdf

Method for converting CWEEDs weather files to EPW format for multiyear simulation of building thermal dynamics - by CY Siu and Z Liao
https://www.sciencedirect.com/science/article/pii/S2215016120302363
