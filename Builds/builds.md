# Builds

There are few builds available in the [Builds](../Builds/) directory.
Changed WLED version 0.14.4. It is a custom build with some features disabled and some added. Compiled for ESP32-C3.

here is a sample of the custom platformio.ini file:

```ini
[env:esp32c3_Twinkle-tron]
extends = env:esp32c3dev
build_flags =
  # Pins
  -D VOLTAGE_PIN=0
  -D CURRENT_PIN=1
  -D LEDPIN=2
  -D TEMPERATURE_PIN=4
  -D RLYPIN=5
  -D IRPIN=6
  -D BTNPIN=7
  
  # Components
  -D WLED_DISABLE_INFRARED ;saves a lot of flash
  -D USERMOD_POWER_MEASUREMENT
  # Temperature
  -D USERMOD_DALLASTEMPERATURE
  -D USERMOD_INTERNAL_TEMPERATURE

lib_deps = ${env.lib_deps}
  paulstoffregen/OneWire@~2.3.7

```
