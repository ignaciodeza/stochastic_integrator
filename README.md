# Stochastic Integrator
A package for integrating stochastic differential equations in an arbitrary number of spatial and parameter dimensions.

If you are a scientist you probably learned to program in Fortran or C, and the most common use for your programming is integrating differential equations, usually you write your own integrating algorithms (from the nastiest Euler to a full Runge-Kutta) and you handle things like coupling, adding noise, Ensembles and seeing how the system reacts when changing one of many parameters, etc.. in an artisanal fashion. Then the program becomes complex, you get the results and for the next proyect you begin all over again, from scratch. Ok, maybe this is not you but it can be somebody you know, and this is where this program fills the gap.

This program allows to integrate a multi-dimensional array of stochastic ordinary differential equations in an arbitrary number of dimensions in an easy way. It has already tested integration algorithms, allows to use gaussian and non-gaussian white and colored noise and to keep everyhting in order so the program will not become chaotic.


You only have to follow the follwing steps:
  1- Edit public.cpp and fill the well documented functions with your equations and parameters.
  2- Edit the configuration file with the parameters you need.
  3- from a terminal situate yourself on the program's main directory and type "make clean; make"
  4- run the program as "stochastic_inegrator config_file" (where config_file is the name of the configuration file you edited in the second step and is situated in the same directory
  5- The program will generate a file in the NetCDF format. This file will contain all the information calculated, no averaging, no losing data. This file can be later analyzed with another program or with a GISS program. we recomend Panoply from NASA (https://www.giss.nasa.gov/tools/panoply/download/)
  
  The program comes with several examples and some python scripts for analysis.
  
  #Instalation of needed netcdf libraries
  
  First you need to install netcdf. This can be downloaded from 

https://www.unidata.ucar.edu/downloads/netcdf/index.jsp

Please note you need to download and install BOTH the c and c++ versions of the program.

to install them, from the terminal, on each directory (beginning with the c version) just type
./configure
make
sudo make install

Once this is installed you should be able to successfully compile the stochastic_integrator.




