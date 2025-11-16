# TOF_Sensor_Test
Contains code and results of testing time of flight (ToF) sensor performance vs. ultrasonic performance.

Note: The following information can also be found in the document titled "Ultrasonic vs. ToF Sensors", also located within this repository.

## Introduction
In its current configuration, the Zotbin utilizes an ultrasonic sensor to measure fullness by emitting sound and measuring the time it takes for the echo to return. In contrast, a time-of-flight (ToF) sensor/camera emits infrared light and measures the time it takes for the reflected light to return, or calculates distance via phase shift. We will evaluate the pros and cons of replacing the current ultrasonic sensor setup with one that includes a ToF sensor instead.

## Performance Metrics
| Trial | Actual (cm) | Ultrasonic (cm) | ToF (cm) |
|-------|-------------|------------------|-----------|
| 1     | 5           | 5.54             | 4.90      |
| 1     | 5           | 5.56             | 5.20      |
| 1     | 5           | 5.97             | 5.00      |
| 1     | 5           | 5.54             | 5.50      |
| 1     | 5           | 5.54             | 4.90      |
| 1     | 5           | 5.54             | 4.90      |
| 1     | 5           | 5.56             | 5.00      |
| 1     | 5           | 5.45             | 5.20      |
| 1     | 5           | 4.61             | 4.90      |
| 1     | 5           | 5.97             | 5.20      |
| 2     | 10          | 11.64            | 10.10     |
| 2     | 10          | 9.95             | 10.10     |
| 2     | 10          | 9.95             | 10.00     |
| 2     | 10          | 11.64            | 9.90      |
| 2     | 10          | 14.10            | 9.90      |
| 2     | 10          | 12.83            | 10.00     |
| 2     | 10          | 11.64            | 10.30     |
| 2     | 10          | 12.40            | 10.00     |
| 2     | 10          | 12.40            | 10.20     |
| 2     | 10          | 11.99            | 10.00     |
| 3     | 15          | 15.98            | 15.40     |
| 3     | 15          | 15.98            | 14.80     |
| 3     | 15          | 15.98            | 14.90     |
| 3     | 15          | 15.97            | 15.00     |
| 3     | 15          | 15.54            | 15.00     |
| 3     | 15          | 15.54            | 15.20     |
| 3     | 15          | 15.56            | 14.90     |
| 3     | 15          | 17.17            | 15.20     |
| 3     | 15          | 17.58            | 15.20     |
| 3     | 15          | 17.60            | 15.40     |

### Ultrasonic Sensor
| Trial | Mean (cm) | Std Dev (cm) | Median (cm) |
|-------|-----------|---------------|--------------|
| 1     | 5.58      | 0.38          | 5.55         |
| 2     | 11.86     | 1.25          | 11.82        |
| 3     | 16.29     | 0.83          | 15.98        |

### Time of Flight (ToF) Sensor
| Trial | Mean (cm) | Std Dev (cm) | Median (cm) |
|-------|-----------|---------------|--------------|
| 1     | 5.07      | 0.20          | 5.00         |
| 2     | 10.05     | 0.127         | 10.00        |
| 3     | 15.10     | 0.21          | 15.10        |

## Conclusion
The Time of Flight (ToF) sensor is significantly more accurate than the ultrasonic sensor. This is evident through the data shown above. Although the measurements were generally smaller than realistic measurements in the ZotBin environment, scaling up the measurements will only make the difference in errors more evident. Additionally, there appears to be adequate library support through the Adafruit or the Pololu libraries for the ToF sensor that is available in the ZotBins lab (links below).
