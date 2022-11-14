# Delayed Mode Quality Control

## Sensor drift and biofouling
Biofouling on the glider can affect the angle of attack, mass and drag coefficient, hence the DAC.

At the end of the mission, the calibration can be checked again to check for sensor drift. 
A simulation mission can also be done at various headings (e.g every 45°) to obtain a post-calibration curve that can be applied in DM.

## Flight models
Flight models are used to estimate glider motion through the water from measured pitch, roll, and pressure (e.g., Merckelbach et al. 2010, 2019 for Slocum gliders, Frajka-Williams et al. 2011 for Seaglider, Rudnick et al. 2018 for Spray gliders). 
Tuning the angle of attack used in a flight model is particularly important since the effective angle of attack changes as biofouling accumulates on a glider during a mission (Todd et al. 2017) or when the external configuration of a vehicle is changed. 
For gliders equipped with current meters that record three-dimensional flow relative to the glider at close range, it is possible to estimate the evolving angles of attack and sideslip, which can be used to correct bias in DAC estimates that result from major biofouling (Todd et al. 2017). 
For Seagliders, the DAC accuracy is dependent on flight regressions performed over the first few dives that determine initial lift and drag parameters. 
These parameters should not necessarily be considered fixed for the duration of a mission and regressions should be carried out repeatedly (Bennet et al. 2019, 2021).

One could describe different levels of flight models (with increasing precision): pitch only, pitch + constant angle of attack (implemented in slocum firmware), steady flight model (pitch dependent angle of attack, eg Sherman et al 2001, Merckelbach et al 2010, Frajka-Williams 2011), dynamic flight model (Merckelbach et al 2019).

## Surface drift correction
Finally, surface drift should be estimated from successive GPS fixes during pre- and post-dive surface intervals. 
The displacement of a glider while on the surface after its final pre-dive GPS fix and before its first post-dive GPS fix should then be subtracted from the displacement between those two GPS fixes; dive duration should be similarly adjusted relative to the time between pre- and post-dive GPS fixes.

For Spray it takes about  60 s for the wing to rotate to vertical to get a GPS fix. 
This correction tends to be small. 
This correction is mentioned in the Appendix of {cite:t}`rudnick2018depth`.

## Quality Control, inter-comparison
Here we might outline some sanity checks from DAC magnitude, EM flow meters and ADCP first bins to make sure drag is correctly estimated, (and DAC orientation for compass calibrations)

