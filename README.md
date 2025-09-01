
Automatic tool for calculating growth rates from new particle formation events in particle sizes of 3-1000 nm. Three methods are used: mode fitting, maximum concentration and appearance time. DMPS data with 30 minute resolution is assumed.

The main.py file contains parameters that can be changed by the user. Please make sure you have all the needed Python packages downloaded and that you have the codes and datasets in the same folder.

This tool uses Janne Lampilahti's aerosol functions package:
https://github.com/jlpl/aerosol-functions

## How to use the code

You need data in netCDF file, with 30 minutes resolution. An example file is provided ("Nanjing.nc"). To run a simulation:

> python3 main.py -f Nanjing.nc -s 2011-12-02 -e 2011-12-03

or alternatively:

> python3 main.py -f Nanjing.nc -s 2011-12-02 -d 2

This command calculates growth rates between Dec 2nd and 3rd (including the end date). If events were found with at least two methods, they are plotted and summarized in the output file.

Print complete list of command line options with :

  > python3 main.py -h
