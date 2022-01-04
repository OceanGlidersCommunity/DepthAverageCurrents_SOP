# Introduction

This standard operational practice (SOP) document for Depth Averaged Currents (DACs) aims to guide the user through the whole glider preparation, deployment, recovery and data processing cycle. 
It aims to result in high quality data and further ensures a data flow both for real time data delivery and long term data archiving.


## Key references
*Table 1*

|  Reference  |  Platform  |  Link |
|---|---|---|
| Rudnick, D. L., Sherman, J. T., & Wu, A. P. (2018). Depth-average velocity from Spray underwater gliders. Journal of Atmospheric and Oceanic Technology, 35(8), 1665-1673. | Spray (flight) | https://doi.org/10.1175/JTECH-D-17-0200.1 |
| Todd, R. E., Rudnick, D. L., Sherman, J. T., Owens, W. B., & George, L. (2017). Absolute velocity estimates from autonomous underwater gliders equipped with Doppler current profilers. Journal of Atmospheric and Oceanic Technology, 34(2), 309-333. | Spray (comparison of DAC and ADCP) | https://doi.org/10.1175/JTECH-D-16-0156.1 |
| Merckelbach, L. M., & Carpenter, J. R. (2021). Ocean glider flight in the presence of surface waves. Journal of Atmospheric and Oceanic Technology. | Slocum (flight) | https://doi.org/10.1175/JTECH-D-20-0206.1 |
| Merckelbach, L., Berger, A., Krahmann, G., Dengler, M., & Carpenter, J. R. (2019). A dynamic flight model for Slocum gliders and implications for turbulence microstructure measurements. Journal of Atmospheric and Oceanic Technology, 36(2), 281-296. | Slocum (flight) | https://doi.org/10.1175/JTECH-D-18-0168.1 |
| Merckelbach, L., Smeed, D., & Griffiths, G. (2010). Vertical water velocities from underwater gliders. Journal of Atmospheric and Oceanic Technology, 27(3), 547-563. | Sloum (flight) | https://doi.org/10.1175/2009JTECHO710.1 |
| Merckelbach, L. M., Briggs, R. D., Smeed, D. A., & Griffiths, G. (2008, March). Current measurements from autonomous underwater gliders. In 2008 ieee/oes 9th working conference on current measurement technology (pp. 61-67). IEEE. | Slocum (flight) | https://doi.org/10.1109/CCM.2008.4480845 |
| Davis, R. E., Kessler, W. S., & Sherman, J. T. (2012). Gliders measure western boundary current transport from the South Pacific to the equator. Journal of Physical Oceanography, 42(11), 2001-2013. | Spray (flight) | https://doi.org/10.1175/JPO-D-12-022.1 |
| Sherman, J., Davis, R. E., Owens, W. B., & Valdes, J. (2001). The autonomous underwater glider" Spray". IEEE Journal of Oceanic Engineering, 26(4), 437-446. | Spray (flight) | https://doi.org/10.1109/48.972076 |
| Frajka-Williams, E., Eriksen, C. C., Rhines, P. B., & Harcourt, R. R. (2011). Determining vertical water velocities from Seaglider. Journal of Atmospheric and Oceanic Technology, 28(12), 1641-1656. | Seaglider (flight) | https://doi.org/10.1175/2011JTECHO830.1 |
| Bennett, J., Stahr, F., & Eriksen, C. (2019). Determining Seaglider Velocities Automatically. | Seaglider (flight) | http://hdl.handle.net/1773/44948 |
| Bennett, J. S., Stahr, F. R., Eriksen, C. C., Renken, M. C., Snyder, W. E., & Van Uffelen, L. J. (2021). Assessing Seaglider Model-Based Position Accuracy on an Acoustic Tracking Range. Journal of Atmospheric and Oceanic Technology, 38(6), 1111-1123. | Seaglider (flight) | https://doi.org/10.1175/JTECH-D-20-0091.1 |
| Eriksen, C. C., Osse, T. J., Light, R. D., Wen, T., Lehman, T. W., Sabin, P. L., ... & Chiodi, A. M. (2001). Seaglider: A long-range autonomous underwater vehicle for oceanographic research. IEEE Journal of oceanic Engineering, 26(4), 424-436. | Seaglider (flight) | https://doi.org/10.1109/48.972073 |


## What are DACs?
Underwater gliders provide an estimate of the depth-average horizontal ocean currents (DAC) between each surfacing during a mission (Fig. 1). 
These estimates are generally produced by dividing the difference in measured displacement during a dive and the displacement through the water estimated from a model of glider flight by the duration of the dive (Eriksen et al. 2001, Webb Research Slocum manual 2005, Rudnick et al. 2018).
DAC estimates are the starting point for most glider-based estimates of absolute horizontal currents. 
DAC contains not only geostrophic currents but also ageostrophic currents including internal tide, inertial current, surface Ekman currents, etc.

- add own Figure / schematic i.e. merge Figure Merckelback 2008 and Rudnick 2018

## Flight models

### Seaglider
Seagliders (and Deepgliders) estimate a Depth Average Current (DAC) as the difference between GPS-tracked over ground and dead-reckoned displacement. 
This estimate relies on an accurate determination of through-water displacement, principally estimated using compass heading, vehicle pitch, variable buoyancy engine position, and vertical velocity measurements along with the Seaglider flight model. 
To briefly summarize Eriksen et al. 2001, Frakja-Williams et al. 2011, Bennett et al. 2019, and Bennett et al. 2021, this flight model employs multivariate regressions to determine vehicle-specific flight parameters including lift and drag coefficients as well as vehicle reference volume during steady flight (accelerations during variable buoyancy engine operations and turns are excluded by the regressions).
Assuming steady flight, a balance between lift, drag, and buoyancy forces, this regression seeks to minimize the difference between measured and estimated glider vertical velocity while determining the vehicle’s angle of attack. 
Given the obtained flight parameters, the momentum-balance equations of the buoyancy-pitch flight model then can be used to estimate vehicle speed and displacement both during steady flight and accelerations at the beginning and apogee of the profile.

This model is used both during and after missions to obtain optimal flight parameters and/or reprocess dive-climb cycles as needed, recognizing that certain parameters may change as a mission progresses. 
After a dive-climb cycle is completed, the DAC estimate is tagged at the midpoint location and time between surfacings, generally dive apogee where the vehicle reaches a maximum dive depth. 
Recent independent measurements of glider velocities via onboard velocimeter (Bennett et al. 2019) and acoustic tracking range (Bennett et al. 2021) have aided in the development of an improved automated flight model system capable of recommending updated flight parameters in near-real time as a mission progresses. 
Independent of these adjustments, however, results confirm the cross-track component of the DAC, used to estimate depth-dependent geostrophic flows, to be accurate within 1 cm/s. 

The basestation processing code, including the automated flight model system (FMS), has been made available to the commercial manufacturer.


### Spray
- XXX

### Seaexplorer
- XXX

### Slocum
- XXX


