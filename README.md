# Examining-Blended-Light-Curves

### Current Work

Gyrochronology is the study of how the age of a star affects the rotation rate. The hypothesis in gyrochronology states that as the star ages, the rotation rate of the star should decreased due to many factors causing a loss of angular momentum. One way to test this hypothesis would be to look at binary stars and calculate thier rotation rate. We can assume that the stars that contain a binary system are born at the same time since capture of one star by another is highly improbable. 

In many cases of binary stars, there is an angular resolution of 0 between the two stars. This means that when space equipment, such as a telescope, makes observations of these binary stars, the observations are actually of two separate stars. This can pose a problem on the analysis side since the signal from each individual star is blended together. Therefore, determining characteristics of each individual star becomes difficult.

In this code, we utilize Dr. Zach Claytor's python implementation called "Butterpy" to create synthetic starspot evolution models and their corresponding light curves. From there, light curves of different stars of varying rotation rate and temperature can be synthesized and blended. It is known that flux changes with respect to temperature to the fourth. Therefore, when blended the two light curves, the flux of the hotter star will be scaled based on the following equation,

${ F = \left( \frac{T_1}{T_2} \right )^4 }$,

where ${T_1}$ represents the temperature of the hotter star and ${T_2}$ represents the temperature of the cooler star. With the blended light curves, we can now use the Lomb Scargle to pull out the underlying rotation rates and plot in a power spectrum. However, stars can come in varying brightness depdending on their temperature, size, and other characteristics. Due to this, the signal from hotter stars can drown out that of the cooler star. Therefore, it is important to understand the boundary in which independent signals can be acquired. 

### Future Work

Now that blended light curves can be synthesized with varying rotation rates and temperatures, we can now create a training set to train a machine learning model, such as a neural network, to determine the rotation rate of the two blended lightcurves. 

### References

ALL BUTTERPY CODE BELONGS TO ZACH CLAYTOR. YOU CAN FIND MORE ABOUT HIS CODE AT THE FOLLOWING URL:

https://github.com/zclaytor/butterpy
