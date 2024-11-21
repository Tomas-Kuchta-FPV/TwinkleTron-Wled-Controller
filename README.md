# LED Pixel Driver (TwinkleTron)

>Toto je anglická verze souboru README. Český překlad je [zde](CZ/README.md).

This project is an open-source controller for addressable LED strips, combining a wide range of features such as power measurement, IR sensors, and easy integration into various installations. The project is designed with a focus on low power consumption and user safety.

Includes:

- **ESP32-C3-WROOM-02** as the main processor.
- Integrated power measurement (ACS722 and voltage divider).
- Relay for LED power control.
- Surge and ESD protection.

<img src="Images/V1/Board_2.jpg" alt="Board Image" width="500" style="border-radius: 50px;"/>

## Table of Contents

0. [Introduction](#led-pixel-driver)
1. [What makes this project interesting?](#what-makes-this-project-interesting)
2. [Features](#features)
3. [Why did I decide to create this project?](#why-did-i-decide-to-create-this-project)
4. [Development](#development)
5. [Documentation](#documentation)
6. [Would I like to sell it?](#would-i-like-to-sell-it)
7. [What is my motivation?](#what-is-my-motivation)
8. [What have I learned?](#what-have-i-learned)
9. [What is its actual use?](#what-is-its-actual-use)
10. [Software](#software)
11. [Conclusion](#conclusion)
12. [Contributions](#contributions)
13. [License](#license)

### Status

- **Version**: 2.0 in the works. Evherything should be ready to order and test.

## What Makes This Project Interesting?

Power measurement!  
I wanted to know how much energy I was consuming, so I decided to use ACS722 and a voltage divider. However, I haven’t seen a similar project that includes this kind of measurement.

## Features

- ESP32-C3-WROOM-02
- Onboard relay for minimal standby current
- Integrated 10A fuse for LED strip protection
- Power measurement using WLED usermod (ACS722, voltage divider)
- Input for an external button
- Temperature sensor
- IR sensor

<details>
    <summary>Show More</summary>
    <ul>
        <li>Easy-to-use screw terminals (default)</li>
        <li>Compatible with PhoenixContact PCB connector</li>
        <li>ESP protection (PTC resettable fuse, ESD protection, diodes)</li>
        <li>Surge protection for 5V and 3.3V</li>
        <li>Boot button can be used as a WLED button</li>
        <li>Buck converter powered from Vin</li>
        <li>Unused GPIOs are exposed on the board</li>
        <li>USB-C connector</li>
        <li>5V logic output</li>
    </ul>
</details>

## Why Did I Decide to Create This Project?

I wanted to build something of my own—something I could improve and customize as needed. I also wanted to contribute to the open-source community and to create something properly designed.  
This project includes several motivations:

- **Power measurement**: To monitor energy consumption.
- **Relay**: To disconnect LED strips.
- **Low standby power**: To minimize energy usage in standby mode.
- **Ease of integration**: To simplify use in various installations.
- **To learn**: To gain experience with new technologies.
- **To share**: To contribute to the open-source community.
- **To create something nice**:  To have a functional and visually appealing solution.

## Development

I've been working on this project for quite a while.

The first prototype didn’t look great, but it worked well despite forgetting to power the SN74AHCT125 IC—something I fixed with a solder bridge.

Version V0.31 was the first to include all desired features but had a few bugs.

V1.0 was the first fully functional version but still had issues, like components on both sides of the PCB causing assembly difficulties and a suboptimal USB-voltage mixer.

V2.0 addressed all known issues and is fully functional. It is still in development, but it feels complete—though you never know what might come up. 😅

## Documentation

A great beginer video can be found here [YouTube](https://www.youtube.com/watch?v=FvPuiWTE6ic).

KiCad files are in the [Board](Board/) directory.

Schematics and PCB layouts are in the [Documentation](Documentation/) directory.  
And the [Builds](Builds/) directory contains the binary for the ESP32-C3.

The enclosure is in the [Case](Case/) directory.  
Photos of the completed project are in the [Images](Images/) directory.

## Would I Like to Sell It?

Yes, in the near future, I would like to sell this project as a finished product so that everyone can use this controller.  
It would also enable me to continue its development and create interesting new projects.

## What Is My Motivation?

- Installing LED strips in 2021.
- Problems with ESP32 (damaged power, failed updates).
- Creating a robust and user-friendly solution.

<details>
<summary>More</summary>
In 2021, I installed addressable LED strips for the first time and was amazed. However, working with bare ESP32 boards came with problems. My first controller released "magic smoke" after I accidentally applied 12V to a GPIO pin. The second ESP32 got damaged while fixing an update while still powered. These experiences inspired me to start this project.
</details>

## What Have I Learned?

I’ve learned a lot, including:

- PCB design  

<details>
<summary>More</summary>

- Using ACS722  
- Using a voltage divider  
- Using an IR sensor  
- Using a temperature sensor  
- Using a relay  
- Using a USB-C connector  
- Using a buck converter  
- Using ESP32-C3  
- Using WLED  
- Using PlatformIO  
- Using ESP-IDF  

I learned how to combine all these into a functional solution—and I enjoyed the process. 😀
</details>

## What Is Its Actual Use?

- **Controlling addressable LEDs**: Precise control of individual LEDs.
- **LED light shows**: Ideal for creating dynamic effects.  
- **Holiday decorations**: Perfect for festive displays.  
- **Easy integration**: Fits into various DIY projects.  
- **Smart home**: Great for lighting automation.

## Software

I use the `WLED` project, which is very user-friendly and feature-rich. You can download the binary [here](Builds/). My usermod is included in [GitHub PR #4108](https://github.com/Aircoookie/WLED/pull/4108). Apologies for any mistakes—I appreciate feedback. Also, I’m not experienced with Git, so I welcome patience with any errors in my PRs.

## Conclusion

This project has been both a challenge and an opportunity to push my skills forward. I’ve learned many new technologies and methods while creating a functional solution I’m proud of. The process confirmed that sharing knowledge and embracing open technologies hold great potential.

I hope this project inspires others and saves time for their own ideas. I welcome feedback, improvement suggestions, or support to continue developing this project.

Thank you for your interest I’m excited about what the future holds!

### Why Am I Doing This?

Honestly, I’m not sure I just felt inspired and supported by my family! This open-source project was born from that.

## Contributions

If you have ideas for improvements or spot errors, feel free to open a pull request or issue. All help is welcome. :)  
If anyone would like to participate in the development, I would be glad for any help. 😊  
And if anyone would like to support me financially for further development not just this project, I will be glad for any help. 😊

## License

The project is currently licensed under **CC BY-NC-SA 4.0**, allowing sharing and modifications for non-commercial use. A future transition to **CERN-OHL-S** is planned after recovering development costs.

**CC BY-NC-SA 4.0** [(CC)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en) **→** **CERN-OHL-S** [(OSI Approved OSHW License)](https://opensource.org/license/cern-ohl-s)

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg


#### Disclaimer (No Warranty)

This licensed work is provided "as is," without any warranties, including implied warranties of merchantability or fitness for a particular purpose. The author(s) and copyright holder(s) bear no liability for claims, damages, or other liabilities.

#### AI Assistance

I used AI to assist with translation and grammar corrections. Thank you for understanding.
