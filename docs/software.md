# Software Design

## Linux

[Linux Kernel Organization](https://kernel.org/) (US non-profit)

## Free TLS Certificates

[Let's Encrypt](https://letsencrypt.org/) (US non-profit)

## Domain Name Registrar

[Namecheap](https://www.namecheap.com/)

## Resources

### General

Description | Link
---|---
The Art of Unix Programming (Raymond) | [WEB ARCHIVE](https://archive.org/details/ost-computer-science-the_art_of_unix_programming-1)
Operating Systems: Three Easy Pieces (Remzi, Andrea)  | [WEB](https://pages.cs.wisc.edu/~remzi/OSTEP/)
Network Programming Guide (beej) | [WEB](https://beej.us/guide/bgnet/)
Site Reliability Guides (Google) | [WEB](https://sre.google/books/)
Advanced Software Design Articles (Mirdin) | [WEB](https://mirdin.com/newsletter-and-blog/)

### C++

Literature:

Description | Link
---|---
Technical Report on C++ Performance (ISO, 2006) | [PDF](https://www.open-std.org/jtc1/sc22/wg21/docs/TR18015.pdf)
Thriving in a Crowded and Changing World: C++ 2006–2020 (Stroustrup) | [PDF](https://web.archive.org/web/20210717062203/https://www.stroustrup.com/hopl20main-p5-p-bfc9cd4--final.pdf)
Joint Strike Fighter AV C++ Coding Standards (2005, Lockheed Martin) | [PDF](http://www.stroustrup.com/JSF-AV-rules.pdf)
C++ Style Guide (Google) | [WEB](https://google.github.io/styleguide/cppguide.html)

Libraries:

Description | Link
---|---
Boost: free peer-reviewed portable C++ source libraries (STRONG RCMD) | [WEBSITE](https://www.boost.org/)

### Python

Description | Link
---|---
Python3 Virtual Environments | [WEB](https://docs.python.org/3/tutorial/venv.html)

### C

Description | Link
---|---
JPL Institutional Coding Standard for the C Programming Language (2009, NASA) | [PDF](http://web.archive.org/web/20190219155254/http://lars-lab.jpl.nasa.gov/JPL_Coding_Standard_C.pdf)
The Power of Ten - Rules for Developing Safety Critical Code (2006, NASA) | [PDF](https://spinroot.com/gerard/pdf/P10.pdf)
C Coding Guidelines for Critical Systems (2004, MISRA) | [PDF](http://caxapa.ru/thumbs/468328/misra-c-2004.pdf)

### Assorted

Description | Link
---|---
Process vs Thread Based PostgreSQL | [HackerNews](https://news.ycombinator.com/item?id=36393030)
ROS2 Real-Time Design | [WEB](https://design.ros2.org/articles/realtime_background.html)
Build System: Future Plans for Autotools | [HackerNews](https://news.ycombinator.com/item?id=25910496)

## Key Knowledge

**Data (its physical storage, idea representation, input/output transformation) is the foundation of all software design.**

Function | Item
--|--
Main Languages | Python (fast abstract), C++ (high-performance complex), C (high-performance), Rust (high-performance reliable-dev), PHP (fast web)
Programming Paradigms | Procedural, Functional, Object-Oriented
Code | Source Code, Assembly Code, Object Code, Byte Code, Machine Code, Executable File, Library File
Runtime | Compiled vs Interpreted, Process and Thread, 
Data Landscape | Kernel Data in RAM, Files and Folders in DISK (filesystem), Program in RAM, Program Data in RAM

## Tools

### Main IDE

(integrated development environment)

[Visual Studio](https://visualstudio.microsoft.com/) (RECOMMENDED)

Free IDE from Microsoft with versatile plugins and collaborative editing.

Workflow:

1. Create project folder with version control and build system

```
git init newproject 
```

2. Prepare the internal file/folder structure

### Compiler

GCC (GNU C compiler) (C/C++/Objective-C/Fortran/Ada/Go/D) --- [GCC Website](https://gcc.gnu.org/)

Clang/LLVM --- [Clang/LLVM Website](https://clang.llvm.org/)

### Text Search

CLI Text Search | [Silver Searcher](https://geoff.greer.fm/ag/), [Silver Searcher on Github](https://github.com/ggreer/the_silver_searcher)

```
# AG Search
ag target-phrase ~/target-folder/
```

## Design Targets

## Operating System

Our preferred kernel is Linux and our preferred operating system is Debian. We're fully committed to this open-source kernel+OS ecosystem for all of our CPU/MPU modules. We use real-time Linux for time-sensitive applications.

We use embedded RTOS (ex. FreeRTOS) for our MCU modules. 

### Linux

Description | Link
---|---
Linux Kernel Website | [WEB](https://kernel.org/)
Real Time Linux, Main Website | [WEB](https://wiki.linuxfoundation.org/realtime/start)

### Debian

Description | Link
---|---
Debian Main Website | [WEB](https://www.debian.org/)
Debian Packages | [WEB](https://www.debian.org/distrib/packages)
Debian Bookworm Release (2023-06-10) | [WEB](https://www.debian.org/News/2023/20230610)
Antivirus | [Debian Manual](https://www.debian.org/doc/manuals/securing-debian-manual/ch08s08.en.html)

### FreeRTOS

[FreeRTOS, Main Website](https://www.freertos.org)

## Codebase

### Version Control

[Git](https://git-scm.com/) (STRONG RCMD)

[Canonical Project Structure (Code Synthesis)](http://open-std.org/JTC1/SC22/WG21/docs/papers/2018/p1204r0.html)

[Github](https://github.com/) (RCMD)

### Build System

Options: make, cmake, meson/ninja

Description | Link
---|---
Meson | [WEBSITE](https://mesonbuild.com/) / [GITHUB](https://github.com/mesonbuild/meson)
Ninja | [WEBSITE](https://ninja-build.org/) / [GITHUB](https://github.com/ninja-build/ninja/)

### Logging

[Boost.Log](https://www.boost.org/doc/libs/1_82_0/libs/log/doc/html/index.html)

### Error Handling

(monitoring/detection and repair/recovery)

C++ exceptions ([pros/cons](https://www.boost.org/doc/libs/master/libs/outcome/doc/html/alternatives/exceptions.html)) traditionally avoided in real-time/critical applications because of insufficient tooling support (ex. Lockheed JSF-CPP Standard) and legacy code non-tolerance (ex. Google CPP Standard).

[Boost CPP Outcomes](https://www.boost.org/doc/libs/1_82_0/libs/outcome/doc/html/index.html), [History](https://www.boost.org/doc/libs/1_82_0/libs/outcome/doc/html/history.html), [ABI Stability Guarantee](https://www.boost.org/doc/libs/1_82_0/libs/outcome/doc/html/abi-stability.html)

[Native CPP Expected](https://www.boost.org/doc/libs/develop/libs/outcome/doc/html/alternatives/expected.html)

### Distribution

* Source Code
* AppImage

For our open source projects, we strive to provide an easy process to compile/install/uninstall the code.

For all our software distribution, we strive to provide data-integrity and data-authenticity verification.

## Graphics

[LearnOpenGL](https://learnopengl.com/)

[VulkanTutorial](https://vulkan-tutorial.com/)

VR/AR:

[OpenXR Spec (Khronos Group)](https://www.khronos.org/registry/OpenXR/specs/1.0/html/xrspec.html)

Machine Vision:

[OpenCV](https://opencv.org/)

[DepthAI (Luxonis)](https://docs.luxonis.com/en/latest/)

## Audio

[Pipewire](https://pipewire.org/)

[Alsa](https://alsa-project.org)

Automated Speech Recognition (ASR):

* [DeepSpeech (Mozilla)](https://github.com/mozilla/DeepSpeech)
* [Whisper (OpenAI)](https://github.com/openai/whisper)

## CAN

https://github.com/linux-can/can-utils

https://www.kernel.org/doc/html/latest/networking/can.html

## Wireless

https://wireless.wiki.kernel.org/en/users/documentation/iw

## IT Automation

[Ansible](https://www.ansible.com/), [Ansible Docs](https://docs.ansible.com), 

[Ansible Best Practices](https://docs.ansible.com/ansible/latest/tips_tricks/ansible_tips_tricks.html), [Ansible Sample Setup](https://docs.ansible.com/ansible/latest/tips_tricks/sample_setup.html)

Note: Ansible 7.3 is available as a [Debian-Package (bookworm)](https://packages.debian.org/source/bookworm/ansible) for easy install with apt

Playbook Design: idempotency

## Website

Web Traffic Analytics

[HTMX](https://htmx.org/)

## Notes

All comments shall use inline comment syntax (ex. //).












