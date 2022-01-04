# Pre-deployment operations and calibrations

## Battery degaussing
Degaussing battery packs before installation is recommended. 
After each degaussing of the battery pack, a careful compass calibration needs to be performed in order to take into account the change in the magnetic environment where the compass is located.

## Ballasting requirements
Vehicle: 
- Good ballast to ensure stable flight
- Record accurate mass

## Compass calibration

### Slocum
- XXX

### Seaglider
We used to rely on pre-deployment compass calibrations but now perform it in-situ running two back-to-back dives at the start of the deployment using 2 different pitch and roll combinations.  
We return the collected magnetometer data, then process it offline and upload a hard-iron and soft-iron correction file.  
Eliminates the problem of subsequent hard-iron distortion caused by large magnetic objects like ships and rocks.  
We also measure any residual hard-iron distortions due to battery pack locations and correct for that (typically none on Seaglider, somewhat present for Deepglider).

### Spray
Local magnetic anomalies are measured before every deployment by moving a glider through a wide range of pitches, headings, and rolls in an area free of stray magnetic fields and estimating the local anomaly field through least squares. 
This first-order correction is stored on board the glider. 
A residual heading- and pitch- dependent error with RMS size of 1.5° remains; this residual error curve is recorded and applied in post-processing. 
A constant magnetic declination for the deployment region is stored onboard the glider; spatially varying magnetic declination can be applied in post-processing. 

### Seaexplorer
Here basic recommendations about compass calibration for the seaexplorer: 

The compass have to be calibrated in the following cases:
- After payload hardware modification
- Upon change of mission location
- After a ballasting procedure (because of added lead weights distribution)
- At least once a year.

It is also recommended to: 
- Do the procedure  in an area of undisturbed magnetic field (e.g. forest, on a beach, at sea).
- To level the vehicle
- To know the true north 
- To set the actuators in neutral position

## Compass error
- XXX

## Antifounling
- XXX



