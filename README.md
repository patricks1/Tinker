# Abundance Matching
The two scripts in this repository execute subhalo abundance matching (or SHAM) in two different ways.

## schechter.ipynb
This script executes a "zero-parameter" SHAM, called such because it takes no parameters but the stellar mass function (SMF), although the SMF itself should be considered a parameter. The script has the name "schechter" because plotting the double Schechter function from Baldry et al. (2012) was the first thing I did with it.

Its process is as follows:
(1) Calculate the number-density-to-mass curve for galaxies using the double Schechter function as fit by Baldry et al. (2012)  
(2) Bin and calculate the number densities of dark matter halo masses from the Bolshoi simulation (Kartaltepe et al. 2007)  
(3) Match the abundances of dark matter halos and galaxies of certain masses to plot the stellar-to-halo-mass relation (SHMR)

## 2d_abundance_matching.ipynb
Users can use this as a tool to generate SHMR functions given various values of scatter.

This script executes a "2D abundance matching" process, named such because it takes two parameters, the SMF and the scatter around the mean SHMR. It finds the best-fit parameters for the functional form of the SHMR given by Hudson et al. (2015) so, given a certain scatter, the resulting SMF matches Baldry et al. (2012).

## References
Baldry, I. K., Driver, S. P., Loveday, J., et al. 2012, MNRAS, 421, 621
Hudson, M. J., Gillis, B. R., Coupon, J., et al. 2015, MNRAS, 447, 298
Kartaltepe, J. S., Sanders, D. B., Scoville, N. Z., et al. 2007, ApJS, 172, 320
