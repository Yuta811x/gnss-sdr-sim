# GNSS-SDR-SIM

Extension to gps-sdr-sim to simulate QZSS satellite signals from QZSS navigation data.
But we have not been able to extend the functionality perfectly.
The Almanac data section is set to 0 input so that ionospheric correction delays, etc. are not stored.
The Almanac data section will be revised in the future.

The following is a detailed description of the expanded functionality.
For more information on the basic functionality of gps-sdr-sim, please see the description of the original program!

### Update Details

Baseband signals with mixed navigation messages can now be created from gps and qzss ephemeris data.
The archive for the daily file can 
be downloaded from: https://sys.qzss.go.jp/dod/archives/pnt.html. 

```
Usage: gps-sdr-sim [options]
Options:
  -e <gps_nav>     RINEX navigation file for GPS ephemerides (required)
  -q <gps_nav>     RINEX navigation file for QZSS ephemerides (any)
  -u <user_motion> User motion file in ECEF x, y, z format (dynamic mode)
  -x <user_motion> User motion file in lat, lon, height format (dynamic mode)
  -g <nmea_gga>    NMEA GGA stream (dynamic mode)
  -c <location>    ECEF X,Y,Z in meters (static mode) e.g. 3967283.15,1022538.18,4872414.48
  -l <location>    Lat,Lon,Hgt (static mode) e.g. 30.286502,120.032669,100
  -t <date,time>   Scenario start time YYYY/MM/DD,hh:mm:ss
  -T <date,time>   Overwrite TOC and TOE to scenario start time
  -d <duration>    Duration [sec] (dynamic mode max: 300 static mode max: 86400)
  -o <output>      I/Q sampling data file (default: gpssim.bin ; use - for stdout)
  -s <frequency>   Sampling frequency [Hz] (default: 2600000)
  -b <iq_bits>     I/Q data format [1/8/16] (default: 16)
  -i               Disable ionospheric delay for spacecraft scenario
  -v               Show details about simulated channels
```

### Important Points
1.QZSS and GPS navigation data must be from the same time.

2.GPS navigation data should be from the following sites.

https://cddis.nasa.gov/archive/gnss/data/daily/. 

Differences in navigation data specifications make it impossible to read the data correctly.

### License

Copyright &copy; 2015-2022 Takuji Ebinuma  
Distributed under the [MIT License](http://www.opensource.org/licenses/mit-license.php).
