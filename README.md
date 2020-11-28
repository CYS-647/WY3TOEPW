# WY3TOEPW
This script is to convert historical weather files stored in WY3 format into EPW format so it could be used for building energy simulation. 

# Background
Building Energy Simulation(BES) is a common practice used to compare and evaluate the energy efficiency of different building designs. As part of the commitment in reducing energy usage and carbon emissions related to energy generation and natural gas heating, many jursdications now require building designers to submit building energy models to ensure new proposed buildings will be more energy efficient than a baseline design(which are modelled based on older energy related standards). 

One of the most important inputs for building energy simulation is weather data. Weather data describes the expected external conditions that a building will experience based on its location. The current accepted practice is to use Typical Year weather files(such as TMY- Typical Meteorological Year in the US or CWEC - Canadian Weather for Engineering Calculations in Canada) to run building energy simulation. Typical Year weather files are created based on statistical methods, the goal is to select 12 representatitve months(each month in a calendar year is represented by 1 representative month) from 15 to 30 years of historical weather data. The results of the selection often 
