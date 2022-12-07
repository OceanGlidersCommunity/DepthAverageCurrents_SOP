# Missions execution

## Calibration at sea

### Slocum
Slocum gliders offer the possibility to recalibrate the compass at sea. 
Using an in situ compass calibration function in the glider software, the glider receives a command to calibrate its own compass while deployed and it will do a series of vertical spirals in the water column, saving the raw data from the compass so it can be sent off and processed onshore. 
The data is run through a calibration tool, and if the results are satisfactory, the operator can send the new calibration file back onto the glider for it to use. 
This gives you the ability to do a QC check on the data before it takes effect and to revert back to the old calibration if something goes wrong. 
While the at sea calibration is not thoroughly tested within the community, it is expected to perform fine; however, when there is the option, we recommend calibrating in the lab where the glider can be moved through a wider range of angles. 

## Reference samples

### Seaglider
To ensure accurate DAC estimates, two in-situ compass calibration dives are also recommended at the start of a mission in which the glider flies at varied pitch and roll angles. 
These dives are carried out such that hard and soft iron corrections can be estimated and applied to magnetometer data (for Deepglider, this includes some distortion caused by the battery pack) to account for any residual distortions introduced between assembly and deployment.  

Collection of magnetometer data needs to be enabled during deployment in order to apply compass calibrations in DM processing ($COMPASS_USE,4)


### Spray
Measurements of water velocity relative to a glider from the nearest sampling cells of onboard ADCPs have been used to measure Spray glider motion through the water {cite:p}`todd2017absolute`. 
For gliders that experience severe biofouling, ADCP measurements can be used to determine time-varying angles of attack and sideslip during a mission. 
Use of these varying angles in the flight model (including sideslip as in {cite:t}`todd2017absolute` and Davis et al. 2012) can improve DAC estimates for badly fouled gliders by removing much of the correlation with a glider’s direction of motion.

{cite:t}`rudnick2018depth` describe a platform-independent procedure for estimating the accuracy of glider-based DAC estimates. 
DAC estimates before and after a glider switch directions along a repeated transect are compared. 
This technique is best applied in deep water where the assumption that actual ocean currents are identical before and after a turn is most valid.

Rudnick et al. (2013) show an estimate of the changing drag coefficient of a Spray glider that accumulated biofouling during a 102-day mission as estimated from a flight model. 
{cite:t}`todd2017absolute` show a similar change in the angle of attack from ADCP measurements.

## Piloting recommendations 
Multiple dives between surfacings should be kept at the same depth in order to use the DAC in depth dependent currents calculation. 
Since the DAC estimate is actually a time average of the horizontal currents along a glider’s three-dimensional path between surfacings, interpretation of the DAC estimate as a depth average depends on uniform sampling of the water column between surfacings. 
For a well-trimmed glider with nearly constant vertical velocity during descent and ascent, this is a valid interpretation. 
Multiple dive/climb cycles to the same depth between surfacings, as may take place in shallow water or to minimize the time on the surface in hazardous areas, reduces the temporal and spatial resolution in DAC estimates. 
Dive/climb cycles to different maximum depths between surfacings (e.g., across a bathymetric slope) result in a current estimate that is biased toward the part of the water column in which the glider spends the most time and should not be interpreted as DAC.

During a mission a U-turn procedure should be considered to check the consistency of the DAC before and after the turn as described in {cite:t}`rudnick2018depth`.
Estimates of depth-average currents from gliders have typical accuracies of 0.01-0.02 m s-1 and negligible bias (Eriksen et al. 2001, Davis et al. 2003, Todd et al. 2011, {cite:p}`rudnick2018depth`). 
In the absence of independent measurements for cross calibration (e.g., from a collocated ship or mooring), the accuracy of DAC currents may be assessed by examining the behavior during changes in horizontal sampling direction (e.g., Todd et al. 2011, {cite:p}`rudnick2018depth`).

