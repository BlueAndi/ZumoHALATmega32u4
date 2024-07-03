# ZumoHALATmega32u4 <!-- omit in toc -->

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](http://choosealicense.com/licenses/mit/)
[![Repo Status](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)
[![Release](https://img.shields.io/github/release/BlueAndi/ZumoHALATmega32u4.svg)](https://github.com/BlueAndi/ZumoHALATmega32u4/releases)

Hardware abstraction layer for the Pololu Zumo32U4 robot (see https://www.pololu.com/category/129/zumo-robots-and-accessories).

## Table of content

* [Architecture](#architecture)
  * [The Principle](#the-principle)
  * [Detail](#detail)
* [How to integrate the library?](#how-to-integrate-the-library)
  * [Example](#example)
* [Requirements to your application](#requirements-to-your-application)
* [OLED Display Support](#oled-display-support)
* [Used Libraries](#used-libraries)
* [Issues, Ideas And Bugs](#issues-ideas-and-bugs)
* [License](#license)
* [Contribution](#contribution)

# Architecture

## The Principle
![Principle](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/BlueAndi/ZumoHALATmega32u4/master/doc/uml/Principle.plantuml)

## Detail
![HAL](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/BlueAndi/ZumoHALATmega32u4/master/doc/uml/HAL.plantuml)

# How to integrate the library?
1. Add it to the _platformio.ini_ in your environment to the _lib\_deps_ section:
    ```
    lib_deps =
        BlueAndi/ZumoHALATmega32u4 @ ~0.1.1
    ```

## Example
See [example](/examples/example/) for more detail.

# Requirements to your application
* **REQ-1** The application shall use the Arduino framework.

# OLED Display Support
Pololu provides 2 different displays for the Zumo32U4: LCD and OLED. Per default, the LCD display is used.
In order to use the OLED display instead, `CONFIG_USE_OLED_DISPLAY` must be set to 1 in the `platformio.ini` file.

```ini
build_flags =
    -D CONFIG_USE_OLED_DISPLAY=1
```

# Used Libraries

| Library                                                                 | Description                               | License |
| ----------------------------------------------------------------------- | ----------------------------------------- | ------- |
| [Zumo32U4 library](https://github.com/pololu/zumo-32u4-arduino-library) | Provides access to the Zumo32U4 hardware. | MIT     |
| [ZumoHALInterfaces](https://github.com/BlueAndi/ZumoHALInterfaces)      | The Zumo C++ HAL interfaces.              | MIT     |

# Issues, Ideas And Bugs
If you have further ideas or you found some bugs, great! Create a [issue](https://github.com/BlueAndi/ZumoHALATmega32u4/issues) or if you are able and willing to fix it by yourself, clone the repository and create a pull request.

# License
The whole source code is published under the [MIT license](http://choosealicense.com/licenses/mit/).
Consider the different licenses of the used third party libraries too!

# Contribution
Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in the work by you, shall be licensed as above, without any
additional terms or conditions.
