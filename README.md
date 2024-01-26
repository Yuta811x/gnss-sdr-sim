# GNSS-SDR-SIM

Baseband signals with mixed navigation messages can now be created from gps and qzss ephemeris data.
Please check gps-sdr-sim for basic specifications

https://github.com/osqzss/gps-sdr-sim

For GPS and QZSS ephemeris data, please get Ephemeris(Rinex Extension version) from the following site

https://sys.qzss.go.jp/dod/archives/pnt.html

### Update Details

```
Usage: gnss-sdr-sim [options]
Options:
  -q <gps_nav>     RINEX navigation file for QZSS ephemerides (any)
```

### Important Point
QZSS and GPS navigation data must be from the same time. 

gps-sdr-sim can use nasa's HP ephemeris data, but not this software

### License

Copyright &copy; 2015-2022 Takuji Ebinuma  
Distributed under the [MIT License](http://www.opensource.org/licenses/mit-license.php).
