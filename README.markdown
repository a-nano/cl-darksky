# Cl-Darksky
cl-dakrsky allows you to retrieve the weather via latitude and longitude.
## Usage

Before starting you need specify your API key:

```
(setf cl-darksky:*api-key* "YOUR_BIG_SECRET")
```

- For currently:

```
(cl-darksky:forecast 45.0455 41.9683)
; => (("ozone" . 381.87) ("visibility" . 6.22) ("uvIndex" . 0) ("cloudCover" . 0.92)
;     ("windBearing" . 125) ("windGust" . 18.73) ("windSpeed" . 11.24)
;     ("pressure" . 1019.32) ("humidity" . 0.89) ("dewPoint" . 32.45)
;     ("apparentTemperature" . 27.34) ("temperature" . 35.37)
;     ("precipProbability" . 0) ("precipIntensity" . 0)
;     ("icon" . "partly-cloudy-night") ("summary" . "Mostly Cloudy")
;     ("time" . 1518293286))
```

- For hourly:

```
(cl-darksky:forecast-hourly 45.0455 41.9683)
; => (("data"
;     (("ozone" . 381.93) ("visibility" . 6.22) ("uvIndex" . 0)
;      ("cloudCover" . 0.91) ("windBearing" . 126) ("windGust" . 18.69)
;      ("windSpeed" . 11.29) ("pressure" . 1019.37) ("humidity" . 0.9)
;      ("dewPoint" . 32.63) ("apparentTemperature" . 27.32) ("temperature" . 35.37)
;      ("precipProbability" . 0) ("precipIntensity" . 0)
;      ("icon" . "partly-cloudy-night") ("summary" . "Mostly Cloudy")
;      ("time" . 1518292800))
;     (("ozone" . 381.44) ("visibility" . 6.22) ("uvIndex" . 0)
;      ("cloudCover" . 0.95) ("windBearing" . 122) ("windGust" . 19)
;      ("windSpeed" . 10.88) ("pressure" . 1019.02) ("humidity" . 0.85)
;      ("dewPoint" . 31.3) ("apparentTemperature" . 27.51) ("temperature" . 35.38)
;      ("precipProbability" . 0) ("precipIntensity" . 0) ("icon" . "cloudy")
;      ("summary" . "Overcast") ("time" . 1518296400))
;      ...
```

## Installation
Now available from [Quicklisp](https://www.quicklisp.org/beta/)

```
(ql:quickload :cl-darksky)
```

## Requirements

- You need an API key to use it (https://darksky.net/dev/). Don't worry, you can use it for free.

## Author

- Artemiy Stepanov

## Copyright

Copyright (c) 2018 Artemiy Stepanov

## License

Licensed under the BSD 2-clause License.
