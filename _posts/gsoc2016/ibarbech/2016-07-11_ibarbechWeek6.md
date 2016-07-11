---
layout: post
title: Update State Machine Code Generation in C++
---
Update State Machine Code Generation in C++
===========================================

As "void compute;" no longer necessary, now when a component with state machine is generated the portion of "compute" no exist.

This method can be supress because Its funtion is realized by the state machine.

This portion disappears of files generated:
*	**genericworker.h**
*	**genericworker.cpp**
*	**specificworker.h**
*	**specificworker.cpp**



