title: "Working Summary Q1 2015"
date: 2015-04-01 11:38:47
tags: [Work, Summary]
---

Since I may need to switch team, I can make a brief summary about what I’ve learned after first 3 months in ARM.

## Background

I joined ARM from the beginning of Jan, 2015 as Graduate Compiler Engineering. ARM is a company selling its IP designs, or more generally, design chips. However, softwares designed for ARM platforms generally need to be compiled, in other words, translated to the machine code that ARM chips can understand. Thus, the compiler is what I suppose to work with ( but maybe not for future works ).

## Works
Our team is focusing on GCC development or optimisation for ARM Cortex-R/M chips. Daily tasks including building entire toolchain using trunk version of GCC, regression tests for different platforms, such as Cortex-M0, M4, M7, GCC bug fix, optimisations etc. We also will publish our toolchain for embedded developer who want to use gcc to build programmes for Cortex-R/M chips.

Since I only worked less than 3 months, there are only quite simple tasks assigned to me, such as fixing a bug in test suites in GCC, validations the release version of our toolchain, design a small system to track the code size changes in Newlib ( A implementation of standard C library for embedded systems).

## Techniques
Our works are mainly done on the Linux (Ubuntu for most of us, maybe there is a guy using Debian).

We have a lot script files ( Shell, Python, Perl ) to automate our daily workflow.

The command such as grep, sed, awk are extremely useful daily work. I’m not yet enough familiar with these command.

The VCS used in team is git, it also are very very useful during fixing bugs in GCC and testing, because it will take quite a lot time to build entire GCC even on our i7 desktops.

We use CI as our test and release strategy, uses Jenkins as the tool. Actually I have the plan to switch the building, release framework to Buildbot as HQ is using such tool.

As mentioned before, I was assigned the project to design a small system to track the code size changes in Newlib and some benchmarks results. We uses Tableau as the front end to visualise quite a lot data. In such project, I wrote a Python script mainly generating a .csv file which contains all raw data required. Then another Python script to convert to the required JSON files for the data server. To be honest, there are quite lots of enhancement can be make for there python scripts.

## Future
New team and new project is waiting. Maybe more C++ working, even some SystemC. Not sure yet.




