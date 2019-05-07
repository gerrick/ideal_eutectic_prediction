# ideal_eutectic_prediction
May 6 2019  
This perl exe will predict the eutectic temperature and compositions of a mixture of 2 or more molecules using the ideal approximation. It is executed with the format:  
./exe [molecule 1] [molecule 2] [... more molecules]  
The molecule names cannot have spaces and must corresond to files (with path) that contain the melting temperature in Kelvin and enthalpy of fusion on this first line. Subsequent lines are not read, so they can contain other information as needed (for example, data references, etc).  
For molecule files:  
$ more methane  
90.7 0.94  
melt_T(K) enth_fus(kJ/mol)  
methane  
https://en.wikipedia.org/wiki/Alkane#Melting_points  
$ more ethane  
90. 2.85  
melt_T(K) enth_fus(kJ/mol)  
ethane  
https://en.wikipedia.org/wiki/Alkane#Melting_points  
Then this is the result:  
$ ./ideal-eutectic methane ethane  
********  
eutectic summary: 69.2721957597478 K  
methane mole fraction: 0.680061639479408  
ethane mole fraction: 0.31993839769333  
convergence tolerance in mole fraction: 1e-05  
required 10 iterations to converge within 5.46608363725889e-06  
********  
