---
layout: post
title:  "Imaging Sun at Radio and Microwave Frequencies"
date:   2017-05-31
desc: "A research project under the guidance of professor Raghunath Shevgaonkar, Department of Electrical Engineering IIT Bombay, India"
author: Pranav Sankhe
keywords: "Corona, Electromagnetic Waves, Temperature Profile,"
categories: [Technical Report]
tags: [Sun, Corona, Radiative heat transfer, Solar Atmosphere]
icon: icon-html 
comments: true
---

This is a short excerpt of research work done by me and my friend Krishna Subramani with [Prof. Raghunath Shevgaonkar](https://www.ee.iitb.ac.in/wiki/faculty/rks) during summers of 2017. I was working on the analysis of electromagnetic wave propagation in the solar atmosphere. The final goal was to obtain the temperature image of the sun if viewed in microwave and radio frequency range. I would like to thank Prof.Shevgaonkar for giving me this wonderful opportunity to dwell into the aspects of research involving laws of physics and simulating them using software of which I had no exposure to begin with. I used Python for simulation purposes; specifically libraries like <font face = "monospace" size = "4">Numpy</font> and <font face = "monospace" size = "4">Scipy</font>.

## Abstract 
The electromagnetic waves in solar corona follow strange trajectories owing to the unique distribution of electrons in the corona. The complexity of the distribution poses a challenge to model the apparent brightness temperature of the corona. Explained below is an attempt to explain the detail procedure of how we analyzed the solar coronal electron distribution and obtained the temperature profile of sun. The radiation has been analyzed at frequencies lying in the microwave and radiowave bands. The electron density profile of corona is such that the refractive index is less than one and drops to zero at some radial distance from the sun. The trajectory of rays in such an environment has been found out and by using laws of radiative heat transfer theory, we obtained the brightness temperature of the sun and thus the complete temperature profile of sun. 

## Structure of Solar Atmosphere 
Before getting into the modeling of the solar atmosphere, let's know a bit about its structure. 

Above the convective zone of the solar interior is the solar atmosphere. This is made up of three main layers, the photosphere, the chromosphere and the corona. These are described below.

<div style="display: flex; justify-content: center;">
<img src="https://raw.githubusercontent.com/sabSAThai/sabSAThai.github.io/master/static/assets/img/blog/solar_imaging/solar_structure.jpg" width="60%" height="50%" align="middle">
</div>

#### Photosphere
The lowest layer of the sun's atmosphere is the photosphere. It is about 300 miles (500 kilometers) thick. This
layer is where the sun's energy is released as light.The photosphere is covered by granulation, which represents the tops of convective cells rising from the interior. The concentration of magnetic fields gives rise to the chromospheric network in the layer above the photosphere, the chromosphere. 

#### Chromosphere
The next layer is the chromosphere. The chromosphere emits a reddish glow as super-heated hydrogen burns off.The temperature rises across the chromosphere from 4,500 degrees Kelvin to about 10,000 degrees Kelvin. But the red rim can only be seen during a total solar eclipse.

#### Corona 
The solar corona consists of very tenuous plasma. At times of total eclipse, observations of the corona are possible because radiation from the solar disk is masked by the Moon. What is normally observed is the so-called K-corona.
</br>
Corona has a very special region known as the transition region. The surface of the sun is almost 10,000 degrees Fahrenheit. That’s really hot. But the sun’s corona is over 200 times hotter—millions of degrees Fahrenheit. That’s like the actual flame of a fire being 200 times colder than the air around that fire.
Why would the area around a hot burning mass be hotter than something that is actually closer to the source of heat? And if the corona is so hot, then why doesn’t it heat up the sun’s surface to a similar temperature? 
The answer to these question comes when you sit down to write the tedious equations of balancing the gravitational and radiational forces. This sure is interesting but out of the scope of this article, hence let's not digress.
It has been seen that the structure of the corona is quite varied and complex. Different zones have been immediately classified on the coronal disc. The astronomers usually distinguish several regions, as described below.
- **Active regions**
Active regions are ensembles of loop structures connecting points of opposite magnetic polarity in the photosphere, the so-called coronal loops.

- **Large-scale structures**
Large-scale structures are very long arcs which can cover over a quarter of the solar disk but contain plasma less dense than in the coronal loops of the active regions. The large-scale structure of the corona changes over the 11-year solar cycle and becomes particularly simple during the minimum period when the magnetic field of the Sun is almost similar to a bipolar configuration (plus a quadrupolar component).

- **Filament cavities**
Filament cavities are zones which look dark in the X-rays and are above the regions where Hα filaments are observed in the chromosphere. Filament cavities are cooler clouds of gases (plasma) suspended above the Sun's surface by magnetic forces. The regions of intense magnetic field look dark in images because they are empty of hot plasma. 


## Obtaining the Trajectory of Electromagnetic Radiation 


In the normal background corona, we will adopt the conventional _Bambauch-Allen model_ for the radial distribution of electron density. The model is based on photometry of white light of the corona and zodiac light. 


\\[ N = 1.55\times10^{14}\rho^{-6}(1 + 1.93\rho^{-10})  electrons/m^{3} \\]

Where, \\( \rho \\) is the radial distance from the center of the sun in terms of the solar radius. 

The refractive index \\(\eta \\) for radiation of frequency \\(f = \frac{2\pi}{\omega}\\) in a medium consisting 'N' free \$electrons/m^{3}$, each making $\upsilon$ collisions/sec, is given by: 

\\[ \eta^{2} = 1 - \frac{Ne^{2}}{\epsilon_0m(\omega^{2} + \upsilon^{2})} \\]

Subsituting the expression of 'N' and assuming 'w' >> 'v' (which is a good approximaton), we have:

\\[ \eta^{2} = 1 - 12400f^{-2}\rho^{-6}(1 + 1.93\rho^{-10})  \\]

where f is the frequency ( \\(f = \frac{2\pi}{\omega}\\) ) 

The path of the rays can be calculated using Snell's laws. To be able to apply Snell's law we need to ensure the following points. 
- All the rays lie in the plane containing the center of Sun. 
- For all points in the solar atmosphere, 

From Snell's Law, we obtain

\\[ \eta\rho\sin{i}= a \\]

Where, 'a' is a constant for a ray and'i' is the angle of incidence <br> 

**Note** : 
- The constant "a" represents the distance between the equator(of the sun) and the ray as the ray approaches infinity. 
- The surface of constant refractive index here is spherical in shape.

For any ray like the one shown below, the follwing equation holds good, 

<div style="display: flex; justify-content: center;">
<img src="https://raw.githubusercontent.com/sabSAThai/sabSAThai.github.io/master/static/assets/img/blog/solar_imaging/a=0.5.png" width="50%" height="50%" align="middle">
</div>

\\[ \frac{\rho{d\theta}}{d\rho} = -\tan{i} \\]


Using the above-developed equations, we finally get to our differential equation.. 

\\[ \frac{d\theta}{d\rho} = \frac{-a}{\rho(\eta^{2}\rho^{2} - a^{2})^{1/2}} \\]


The trajectory of ray was obtained by solving the above diifferential eqaution. 
 
This is the python script which simulates the sun's atmosphere and plots the trajectory of the rays. [Click here for the code](https://github.com/sabSAThai/Rate-racing-in-plasma/blob/master/python_scripts/script.py)

Here are the simulation results : 

For ray which made a distance of 0.5 solar radii from the equator and for a beam of rays. 

<div style="display: flex; justify-content: center;">
<img src="https://raw.githubusercontent.com/sabSAThai/sabSAThai.github.io/master/static/assets/img/blog/solar_imaging/traj.png" width="75%" height="30%" align="middle">
</div>

## Obtaining the Temperature profile 
To understand the radiative heat transfer theory, consider a cloud with a hot source of radiation behind it. The radiation will enter the cloud with intensity \\(I_o\\) but will be absorbed on passing through the cloud.

<div style="display: flex; justify-content: center;">
<img src="https://raw.githubusercontent.com/sabSAThai/sabSAThai.github.io/master/static/assets/img/blog/solar_imaging/cloud.png" width="50%" height="20%" align="middle">
</div>

\\( dI = - k_nIdl \\) , <br>
where, I is the intensity entering each volume element, <br> 
\\( k_n \\) is the absorption coefficient, or opacity, <br>
dl is the length element 

The solution to the above differential equation is : 

\\[ I = I_0exp(- \int_{0}^Lk_ndl) \\]

Note that the integration is taken along the line of sight from the observer.  In the case where the absorption is constant, of course, \\(k_n\\) can be brought out of the integral.  The integral quantity is a dimensionless quantity called the _optical depth_ (\$\tau$). The optical depth is a convenient way to refer to the _thickness_ of a cloud. It basically measures how many e-foldings of intensity reduction the cloud's thickness represents.

To obtain a relation between the observed temperature, source temperature and the cloud temperature, we use the _Rayleigh-Jeans approximation_. We obtain the following: 

\\[ T_{obs} = T_{cloud}e^{-\tau} + T_e(1 -e^{-\tau}) \\]

Quite intuitive, isn't it?

The simulation results: 

At Frequency =  18 Megacycle per second. (\\(18\times10^{6} Hertz\\)):

<div style="display: flex; justify-content: center;">
<img src="https://raw.githubusercontent.com/sabSAThai/sabSAThai.github.io/master/static/assets/img/blog/solar_imaging/temp_profile_18MC.png" width="75%" height="25%" align="middle">
</div>


At Frequency =  100 Megacycle per second. (\\(100\times10^{6} Hertz \\)):

<div style="display: flex; justify-content: center;">
<img src="https://raw.githubusercontent.com/sabSAThai/sabSAThai.github.io/master/static/assets/img/blog/solar_imaging/temp_profile_100MC.png" width="75%" height="20%" align="middle">
</div>

At Frequency =  400 Megacycle per second. (\\(400\times10^{6} Hertz\\)):

<div style="display: flex; justify-content: center;">
<img src="https://raw.githubusercontent.com/sabSAThai/sabSAThai.github.io/master/static/assets/img/blog/solar_imaging/temp_profile_400MC.png" width="75%" height="20%" align="middle">
</div>


**Note**: 
We considered a radially symmetric profile of electron density in the solar atmosphere. But actually, the sun has many disturbances in its bizarre atmosphere. One of the type of irregularities is called coronal cone cavity. These are conical shaped regions which have their apex at the core of the sun and they extend up to the outer atmosphere. These conical regions have lesser electron density than their surroundings as the material ejects out from this cones. These ejections(sudden massive outbursts) are the reasons for solar flares. 
When you observe the sun, these regions appear darker than the surrounding area by the virtue of low electron density at the given frequency. 


## Acknowledgments

1. Radio Reflection and Refraction Phenomena in the High Solar Corona, Ronald N. Bracewell \\(\&$\\) George W. Preston, Berkeley Astronomical Department, University of California. 
2. Cloud picture credits: https://web.njit.edu/~gary/728/assets/cloud.gif     



