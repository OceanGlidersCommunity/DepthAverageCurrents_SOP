# Sensors and integrations 

## Compass

|  Manufacturer, sensor  |  Accuracy  |  Slocum |  Spray |  Seaglider |  Seaexplorer |
|---|---|---|---|---|---|
|  PNI, TCM3  |  0.5º  | x |   |   |   |
|  PNI, TCM2.5  |  0.8º  |   | x |   |   |
|  PNI, TCM Prime  |  1º  |   |   | x | x |
|  Sparton, SPD3003D  |  to be documented  |   |   | x |   |

Known issues: 
- Compass calibration needed
- Old Seaglider software (not sure if still current) used to take several seconds to wait for values to converge before returning the final value.

## GPS

- Garmin 15H-W (SeaGlider)
- EB-870 GPS engine board with a JDGA QVA Active GPS Antenna (SeaExplorer)

Known issues: When gliders drift on surface before the first GPS fix, it needs to be corrected. Fix duration / HDOP minimum requirements can be set by users on some glider models.

