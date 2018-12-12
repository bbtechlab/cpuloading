# Utility for checking the performance of your process in embedded Linux.

When you design and implement an application which need to allocate memory, 
create many threads and your process consume a lot of CPU resource at running time. 
If you don't manage memory carefully while you are programming, your process will make
whole program die or suspend without seeing any useful messages after running time.
At that time, you perhaps dont think the reason come from your process because it will 
not happen immediately at running time, only happen after uncertain times (maybe take 1 hours/ days/ etc.).
Therefore, to make sure that you already took care of memory well you use cpuloading utility
to check it

# Clone repository

bamboo@BBTECHLAB:~$ git clone https://github.com/bbtechlab/cpuloading.git
bamboo@BBTECHLAB:~/cpuloading$ tree -L 1 ./
./
├── build_date.c
├── cpuloading.c
├── Makefile
└── README.md

# How to compile

bamboo@BBTECHLAB:~$ cd ~/cpuloading
bamboo@BBTECHLAB:~/cpuloading$ make

# How to test

bamboo@BBTECHLAB:~/cpuloading$ ./cpuloading 10

================================================
   Start CPU Loading v1.0 application
   Copyright (c)BBTECH Lab. http://bbtechlab.com!!
   Build date : Wed Dec 12 18:11:16 +07 2018
   Build user : bamboo@BBTECHLAB
================================================


Usage: ./cpu_loading [count]
CPU LOAD RUNNING FOR COUNT: 10
COUNT:   1      CPU LOADING:    1
COUNT:   2      CPU LOADING:    1
COUNT:   3      CPU LOADING:    1
COUNT:   4      CPU LOADING:    1
COUNT:   5      CPU LOADING:    0
COUNT:   6      CPU LOADING:    1
COUNT:   7      CPU LOADING:    0
COUNT:   8      CPU LOADING:    1
COUNT:   9      CPU LOADING:    1
COUNT:  10      CPU LOADING:    0
AVERAGE:0.700   MAX:1


