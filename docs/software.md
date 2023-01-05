# Software Design

## Languages

These are the main languages that we are most familiar with:

* Python (fast abstract)
* PHP (fast web)
* C (high-performance)
* C++ (high-performance complex)
* Rust (high-performance reliable-dev)

## Resources

[The Art of Unix Programming, e-book](https://archive.org/details/ost-computer-science-the_art_of_unix_programming-1)

Topic | Description | Link
---|---|---
Site Reliability | Google SRE Free Books/Resources | https://sre.google/books/
Build System | Future Plans for Autotools | https://news.ycombinator.com/item?id=25910496
Operating System | Operating Systems: Three Easy Pieces | https://pages.cs.wisc.edu/~remzi/OSTEP/
Antivirus | Debian Manual | https://www.debian.org/doc/manuals/securing-debian-manual/ch08s08.en.html
Dev Setup | Best Programming Setup and IDE, John Carmack and Lex Fridman | https://www.youtube.com/watch?v=tzr7hRXcwkw





## Operating System

All our high-performance compute modules (ex. APU/MPU) run the Linux kernel. Our preferred OS is Debian. We're fully committed to this open-source kernel+OS ecosystem for all of our projects. We use real-time Linux for time-sensitive applications.

All our simple compute modules (ex. MCU) run an embedded RTOS (ex. FreeRTOS).

Topic | Description | Link
---|---|---
[Linux Kernel, Main Website](https://kernel.org/)
[Debian, Main Website](https://www.debian.org/)
[Real Time Linux, Main Website](https://wiki.linuxfoundation.org/realtime/start)
[FreeRTOS, Main Website](https://www.freertos.org)

## Codebase, Version Control, Build System

[Canonical Project Structure (Code Synthesis)](http://open-std.org/JTC1/SC22/WG21/docs/papers/2018/p1204r0.html)

[C++ Style Guide (Google)](https://google.github.io/styleguide/cppguide.html)

[Git](https://git-scm.com/) (strongly recommended)

[Github](https://github.com/)

[Meson](https://mesonbuild.com/)

## Distribution

* Source Code
* AppImage

For our open source projects, we strive to provide an easy process to compile/install/uninstall the code.

For all our software distribution, we strive to provide data-integrity and data-authenticity verification.

## Graphics, VR/AR, Machine Vision

[LearnOpenGL](https://learnopengl.com/)

[VulkanTutorial](https://vulkan-tutorial.com/)

[OpenXR Spec (Khronos Group)](https://www.khronos.org/registry/OpenXR/specs/1.0/html/xrspec.html)

[DepthAI (Luxonis)](https://docs.luxonis.com/en/latest/)

## Audio

[Pipewire](https://pipewire.org/)

[Alsa](https://alsa-project.org)

[DeepSpeech (Mozilla)](https://github.com/mozilla/DeepSpeech)

## C, C++

Thriving in a Crowded and Changing World: C++ 2006–2020 (STROUSTRUP)

[PDF](https://web.archive.org/web/20210717062203/https://www.stroustrup.com/hopl20main-p5-p-bfc9cd4--final.pdf)

Joint Strike Fighter AV C++ Coding Standards, 2005, Lockheed Martin

[PDF](http://www.stroustrup.com/JSF-AV-rules.pdf)

JPL Institutional Coding Standard for the C Programming Language (2009) (NASA)

[PDF](http://web.archive.org/web/20190219155254/http://lars-lab.jpl.nasa.gov/JPL_Coding_Standard_C.pdf)

The Power of Ten - Rules for Developing Safety Critical Code (2006) (NASA)

[PDF](https://spinroot.com/gerard/pdf/P10.pdf)

C Coding Guidelines for Critical Systems (2004) (MISRA)

[PDF](http://caxapa.ru/thumbs/468328/misra-c-2004.pdf)

## Notes

All comments shall use inline comment syntax (ex. //).

## CAN

https://github.com/linux-can/can-utils

https://www.kernel.org/doc/html/latest/networking/can.html

## Wireless

https://wireless.wiki.kernel.org/en/users/documentation/iw












