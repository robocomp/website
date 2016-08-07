---
layout: post
title: RoboCompDSL's Tests
---

Hi!

After develop and following the Software Development Life Cycle:

<img src="http://xbsoftware.com/wp-content/uploads/2014/10/software-development-life-cycle.png" alt="" width="400"/>

I have created an script which contains tests for RoboCompDSL. This script allows generate easy components automatically with
test code and run them. Users just have to supervise and continue with next test if everything works.

This work and more information can be found [here.](https://github.com/robocomp/robocomp/tree/highlyunstable/tools/robocompdsl/tests)

## How does it work?

**tests.sh** has a main with 3 options:

  1.- Tests for CPP components.
  
  2.- Tests for PYTHON components.
  
  3.- Exit. (You can exit by simply pressing *Ctrl + C* too)
  
If you select first or second option, tests.sh will generate and run your components in **/tmp/** directory.
Why /tmp/? Simply, this tests are useless if everything works so in /tmp will not bother and will be removed after reboot.
if you need to work with them, you can find them there or re-launching the script.
  
## Is it nice?
  
Of course, this script works with [Yakuake](https://yakuake.kde.org), and uses it 
to offer a much more pleasant and familiar test environment. It will create and divide tabs for each test.
