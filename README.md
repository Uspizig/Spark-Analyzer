# Spark Analyzer: The Programmable USB-C Power Delivery Analyzer & Power Supply

<p align="center">
<img src="./images/SparkAnalyzer.jpg" width="800" height="444"/>
</p>

This is a modification of Spark Analyser to my personal needs. Please check the oroginal Product here [now](https://www.crowdsupply.com/elektrothing/spark-analyzer).


The **Spark Analyzer** excels in power management. It is a versatile ESP32-powered device tailored for enhancing project development and debugging processes. It is fully compatible with USB-C Power Delivery (PD) and also supports the Programmable Power Supply (PPS) feature, allowing for precise control and management of power. Its compact design facilitates easy inline integration with existing setups, providing essential insights and control over power delivery.

Equipped with WiFi and BLE, the Spark Analyzer offers wireless connectivity, enabling developers to remotely monitor and adjust voltage levels, log data, and analyze power consumption through a user-friendly interface. This design prioritizes convenience and efficiency, removing the need for physical buttons and supporting distance operation.


## Features:

1. **Configure USB Power Delivery PD**: When the Spark Analyzer is connected to a USB port that supports Power Delivery (PD), you can configure the output voltage as 5V, 9V, 15V or 20V.

2. **Configure USB Programmable Power Supply PPS**: When the Spark Analyzer is connected to a USB port that supports Programmable Power Supply (PPS), then you can configure the output voltage between 3.3V and 21V in steps of 20 mV. You can also limit the current up to 3A in steps of 50mA.

3. **Power Analysis**: The Spark Analyzer comes with a current sensor. This allows for accurate current draw measurements, essential for understanding power usage in your projects.

4. **Wireless Control**: Untehther your development process with the Spark Analyzer’s wireless capabilities. With both WiFi and BLE, this tool allows remote control and data logging. Users can adjust settings and monitor data from a distance, offering a more flexible development experience.

5. **Open Source & Programmable**: As an open-source device, the Spark Analyzer offers unmatched versatility. It is fully programmable, allowing you to tailor its functionality to your specific applications. This customization extends to software and hardware, opening up endless possibilities for creative and efficient project development.

6. **Compact Design**: Designed for convenience, the Spark Analyzer's compact and sleek form factor allows for seamless integration into existing setups. Its compatibility with USB PD power sources and inline integration capability minimizes the need for additional equipment or extensive redesign, making it a versatile and user-friendly addition to any development environment.

5. **Safety**: Safety is crucial when working with electricity and is at the heart of Spark Analyzer. An integrated output FET allows for software programmable current limit that switches off the power in high-current scenarios.

6. **Data Storage**: Store your Voltage Curves on SD Card and play back voltage ramps

7. **Display**: Monitor live the current status of the Voltage Source

8. **RTC**: Operate the Device in remote areas without Wifi in Standalone mode and still have a proper Time Monitoring

9. **Air Quality**: Measure the Air Qulity with the BME680: Temperature, Humidity, Pressure and eCO² to take actions based on Enviromental Data

10. **Gyro, ACC**: Identify Movement of the Device and take actions.

## Specifications

#### Power
- **Negotiable Power Delivery**: Options of 5 VDC, 9 VDC, 12 VDC, 15 VDC, 20 VDC; max 5 A (100 W at 20 VDC). It is also PPS compatible up to 21 VDC. Note: the Spark Analyzer comes preinstalled with firmware that supports PD. If you want to use PPS you can load this version instead: [WebApp_PPS](https://github.com/tooyipjee/Spark-Analyzer/tree/master/PlatformIO/WebApp_PPS).
- **USB Type-C Port**: For power delivery and integrated JTAG programming.
- **ON Semiconductor [FUSB302MPX](https://www.onsemi.com/pdf/datasheet/fusb302b-d.pdf)**: Programmable USB Type-C control and USB PD communication.
- **ESD Protection**: On D+/D-/CC1/CC2 pins.
- **Texas Instruments [TPS62175DQCT](https://www.ti.com/product/TPS62175/part-details/TPS62175DQCT)**: 3.3 VDC 0.5 A max output DC-DC Step-Down Converter.
- **Power Output**: 3.5 mm, 2-position terminal block.

#### I/O Configuration
- **GPIOs**: 4 GPIOs (I2C, UART, SPI compatible).
- **Power Pins**: 1x 5 VDC and 1x GND.

#### Microcontroller
- **Model**: [ESP32-S3 Wroom](https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf) 
- **Wi-Fi**: 802.11b/g/n.
- **Bluetooth**: BLE 4.2.
- **Flash Memory**: 4 MB.

#### Interface
- **3x LED Indicators**
  - Power On
  - Output Enable
  - Programmable LED/Debug
- **Buttons**
  - Reset
  - Programmable 2Buttons/Debug
  - Jog Dial

#### Programming
- **RX/TX Pins**: For programming.
- **Micro SD Card**: For recall configuration files.
- **USB-C**: Built-in USB JTAG programmer (ESP32-S3), compatible with Arduino. Select ESP32-S3 Dev Board.

#### Output
- **Current Output**: [CC6904SO-10A](https://datasheet.lcsc.com/lcsc/2304140030_Cross-chip-CC6904SO-10A_C469389.pdf).
- **Current Sensor**: Hall Effect Current Sensor.
- **Output Enable**: [DMP3017SFG-7 FET](https://www.diodes.com/assets/Datasheets/products_inactive_data/DMP3017SFG.pdf).

<p align="center">
<img src="./images/TopDown.jpg" width="600" height="400"/>
</p>


## Spark Analyzer Mobile App

<p align="center">
<img src="./images/App.jpg" width="400" height="800"/>
</p>

> **Note**: The Spark Analyzer Mobile App is currently in active development. The features described below are subject to change as we continue to improve the app.

The Spark Analyzer Mobile App, currently done for [Android](https://play.google.com/store/apps/details?id=com.elektrothing.SparkAnalyzer&hl=en&gl=US) (iOS support is available via [RemoteXY](https://apps.apple.com/us/app/remotexy/id1168130280), is the perfect companion to your Spark Analyzer device. It simplifies monitoring and controlling power delivery with these key features:

- **Voltage Selector**: Easily choose from different voltage levels (5 VDC, 9 VDC, 15 VDC, or 20 VDC) using a user-friendly selector.
- **Output Toggle**: Turn the power output on or off conveniently with a toggle switch.
- **Current Logging**: Save current draw as a .csv file.
- **Current Limit**: Ability to set a software current trip as a safety feature.
- **Read-time Display**: View current set point, current draw and output enable in real time on your phone.

### Key Features:

- **Voltage Selector**: The app comes with a user-friendly voltage selector that allows you to easily choose from the different voltage levels supported by the UCPD protocol. Whether you need 5V, 9V, 15V, or 20V, switching between these options is just a tap away.

- **Output Toggle**: Need to turn the power output on or off? The app features a convenient toggle switch that gives you full control over the Spark Analyzer's output, making it simple to manage your device remotely.

- **Current Draw Chart**: Keep an eye on your project's power consumption with the app's real-time current draw chart. This feature provides a graphical representation of the current being drawn, helping you to monitor and optimize your power usage effectively.

### Future Developments:

The Spark Analyzer Mobile App is continuously being improved, with several new features in the pipeline. Upcoming updates will include the ability to export logs for further analysis, set current limits to prevent overcurrent scenarios, and much more.

## Testing for Performance

At the heart of Spark Analyzer's design is a commitment to reliability and performance. To ensure that Spark Analyzer stands up to real-world demands, we subjected it to testing under use conditions.

### Max Current Test: 3A at 9V
Under a load condition of 3A at 9V, Spark Analyzer showcased its robust power delivery capabilities without any hitches.

<p align="center">
<img src="./images/9V_3A.jpg" width="800" height="450"/>
</p>

### Max Voltage Test: 1.5A at 20V
Even at its maximum voltage output of 20V with a 1.5A load, Spark Analyzer continued to perform seamlessly, demonstrating its versatility and reliability.

<p align="center">
<img src="./images/20V_1.5A.jpg" width="800" height="450"/>
</p>



## License

MIT License

Copyright (c) 2023 elektroThing

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
