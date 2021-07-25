# Design, Software

REV: 2021-07-21

Official Guidebolt Software-Design Guide

## Resources

The Art of Unix Programming

[TEXT](https://archive.org/stream/ost-computer-science-the_art_of_unix_programming-1/the_art_of_unix_programming%20%281%29_djvu.txt) [PDF](https://ia800202.us.archive.org/27/items/ost-computer-science-the_art_of_unix_programming-1/the_art_of_unix_programming%20%281%29.pdf)

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

## Basics

We have different types of software:

* Embedded
* General-Purpose
* 

We like these programming languages:

* Python
* PHP
* C
* C++

Python is good for general-purpose scripting and abstract programming.

PHP is good for fast-deploy web-development. We like the LEMP stack (linux, nginx, mysql, php).

C is good for embedded programming and simpler general-purpose programs.

C++ is good for more complex general-purpose programs with performance optimization.

## Data Management

All source code must be ultimately organized in a single-umbrella-element (file or folder) per software-module. The single-umbrella must be specific to that module.

REASON: A single umbrella element is easier to share, back-up, and reference. It is clear where supporting data should be organized; at the start of the file or within the top folder (ex. README file, docs folder).

All source code must be organized with documentation to make it useful (ex. compile, install, run). This documentation should be proportional to the complexity/specialness of the use-process.

All long-term source-code and supporting-data must be version-controlled with GIT.














