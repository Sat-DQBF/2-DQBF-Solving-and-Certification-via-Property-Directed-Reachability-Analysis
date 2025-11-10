# 2-DQR 

This repository contains the code and benchmarks of 2DQBF -- our implementation of 2-DQBF solver.

The code is based on the results published in the paper:

2-DQBF Solving and Certification via Property-Directed Reachability Analysis\
Long-Hin Fung, Che Cheng, Yu-Wei Fan, Tony Tan, Jie-Hong Roland Jiang\
Proceedings of FMCAD 2024 (best paper award)\
Invited and submitted to Formal Methods in System Designs




# Building 2DQR
- Compile [AVR](https://github.com/aman-goel/avr.git) and have the following structure.
```
avr-2.1
└── build
    ├── avr
    └── bin
        ├── dpa
        ├── reach
        └── vwn

```
- Download and install [vcpkg](https://github.com/Microsoft/vcpkg)
- Run ``${vcpkg root}/vcpkg install boost-process cxxopts z3``
- Go to ``./build``
- Run ``cmake -DCMAKE_TOOLCHAIN_FILE=${vcpkg root}/scripts/buildsystems/vcpkg.cmake .. ; make``

# Usage

```./2dqr --input <input file> [--skolem] [--output <output path>] [--avr <path to avr>] [--help]```
