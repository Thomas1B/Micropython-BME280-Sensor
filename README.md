# Micropython BME280 Module

This is a module the BME280 temperature, pressure and humiditiy, to be used with micropython on the Pi Pico.

## Class Description

`sensor = BME280(SDA, SCL, id=0, FREQ=400_000, mode=BME280_SAMPLE_1, address=BME280_I2CADDR)`

- `SDA` is the pin the used for SDA.
- `SCL` is the pin the used for SCL.
- `id` is the identifies particular i2c device.
- `FREQ` is the maximum frequency for SCL, default 400_000.
- `mode` is the setting for oversampling of the humidity value. It must be either a single int or a tuple of 3 ints, specifying (mode_hum, mode_temp, mode_pressure).
- `address` is the address to the I2C being used.


## Examples 
```py
    sensor = BME280(SDA=16, SCL=17)

    print("Starting Example: ", end=', ' )
    print(sensor.read_temperature(),
          sensor.read_pressure(),
          sensor.read_humidity(),
          sensor.read_altitude(),
          )
```

outputs -> 
`
Starting Example: 18.95 1009.7 53.42 29.1
`

