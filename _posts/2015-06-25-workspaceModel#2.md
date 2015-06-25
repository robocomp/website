---
layout: post
title: New build system and workspace model in Robocomp #2
categories: [ GSoC15]
tags: [nithin]
description: 
---

For managing these components we would need different utilities. So i started compiling a list of different utilities keeping a reference to other frameworks. Finally i have decide on my list

* rc_init_ws  
* rcbuild  
* rced  
* rccd  
* rcrun  
* rccomp  

 For more information about the utilities see my [tutorial]() on build utilities .All the utilities are implemented using python except `rccd` which is implemented as a shell function, As a subprocess cant affect its parents environment. So i was thinking anyway we will need to source a bash script, so we could move the exporting of the environment variables also into that script. 

##Future work

 One useful feature that needs to be implemented is auto complete for the arguments. It would be a very useful feature as we don't need need to know the exact component name, etc. Also some serious work on the manifest.xml has to be done. It was planned to contain basic info on packages like name, maintainer, dependencies etc. I didnt do it right now because i was not really sure about the component dependencies, i will need to discuss about it a bit.