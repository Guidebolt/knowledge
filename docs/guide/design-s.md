# Design, Software

REV: 2021-07-28

Official Guidebolt Software-Design Guide

## Reference

[FreeRTOS](https://www.freertos.org)

## Codebase, Version Control, Build System

[Canonical Project Structure (Code Synthesis)](http://open-std.org/JTC1/SC22/WG21/docs/papers/2018/p1204r0.html)

[C++ Style Guide (Google)](https://google.github.io/styleguide/cppguide.html)

[Git](https://git-scm.com/)

[Meson](https://mesonbuild.com/)

## Graphics, VR/AR, Machine Vision

[LearnOpenGL](https://learnopengl.com/)

[VulkanTutorial](https://vulkan-tutorial.com/)

[OpenXR Spec (Khronos Group)](https://www.khronos.org/registry/OpenXR/specs/1.0/html/xrspec.html)

[DepthAI (Luxonis)](https://docs.luxonis.com/en/latest/)

## Audio

[Pipewire](https://pipewire.org/)

[Alsa](https://alsa-project.org)

[DeepSpeech (Mozilla)](https://github.com/mozilla/DeepSpeech)

## General

The Art of Unix Programming

[TEXT](https://archive.org/stream/ost-computer-science-the_art_of_unix_programming-1/the_art_of_unix_programming%20%281%29_djvu.txt) [PDF](https://ia800202.us.archive.org/27/items/ost-computer-science-the_art_of_unix_programming-1/the_art_of_unix_programming%20%281%29.pdf)

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

SW Types: embedded, general-purpose

Preferred Languages: Python (fast abstract), PHP (fast-deploy web-dev), C (embedded, simple high-rel programs), C++ (complex high-performance programs)

Preferred VCS: Git

## Standards

All source code must be ultimately organized in a single umbrella-element (file or folder) per software project/module. The single-umbrella must be specific to that module.

REASON: A single umbrella element is easier to share, back-up, and reference. It is clear where supporting data should be organized; at the start of the file or within the top folder (ex. README file, docs folder).

All comments shall use inline comment syntax (ex. //).

All source code should be organized with documentation to make it useful (ex. compile, install, run). This documentation should be proportional to the complexity/specialness of the use-process.














