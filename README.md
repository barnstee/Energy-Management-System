## PV-Monitor

PV-Monitor is a simple .NetCore app capturing telemetry data. This is running on Linux on a Raspberry Pi. The telemetry data captured consists of:

1. Weather data from [www.openweathermap.org](http://www.openweathermap.org), as the weather impacts PV performance.
2. Telemetry data from the PV’s inverter (The inverter uses the [Fronius API](https://www.fronius.com/en/photovoltaics/products/all-products/system-monitoring/open-interfaces/fronius-solar-api-json-)). A [SunSpec](https://sunspec.org)-compliant version using ModbusTCP is in the works.
3. Smart meter telemetry data leveraging its [IEC 62056-21 standard](https://en.wikipedia.org/wiki/IEC_62056) optical interface using [a USB reader](https://shop.weidmann-elektronik.de/index.php?page=product&info=24). IEC 62056-21 uses the Smart Message Language - [SML](https://wiki.wireshark.org/SML).
4. Wallbe Wallbox configuration using surplus energy from the PV to charge an Electric Vehicle.

Telemetry is sent to a Microsoft Azure IoT Central application based on the [IoT Central energy app templates](https://apps.azureiotcentral.com/build/energy).
The device template for the app can be found [here](./PV-Monitor.json).
