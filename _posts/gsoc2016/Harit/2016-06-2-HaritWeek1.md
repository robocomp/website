---
layout: post
title: Introduction
---

About myself
============

Hi all, my name is Harit Pandya.I am 4th year PhD student at Robotic Research Center, IIIT Hyderabad, India. My thesis involves implementing Visual Servoing across object instances for a category, path planning of robotic arm. I am also involved in environment perception for autonomous car.
Previously, I worked with Ericsson Global Ltd. Mumbai for 1.5 years, where I was responsible for planning and implementation of 3G(WCDMA) and 4G(LTE) networks for priority customers like Vodafone, Idea and Korea telecom. Please visit [my webpage](http://robotics.iiit.ac.in/people/harit.pandya/) for more details. 

Short description of the project
============

In this project, I consider the problem of object detection using Convolutional Neural Network (CNN) for Robocomp library. The task comprises of two separate components: Firstly, I will integrate current Robocomp repository to work with Caffe library for object recognition. Secondly I will interface simulation environment of RoboComp with the detection framework. Given an image the primary task is to detect the location of the object that will be given by a bounding box around the object. That is followed by classification task where the objective is to  predict the category of the object. Major challenge is object localization in the image. CNNs’ work pretty well for classification tasks, however for object localization edge and contrast based features are used by state-of-art object detection methods that generate object proposals. Another challenge is working with CAD models, since most of the model are low textured hence finding features is difficult for them.
 
Following are the deliverables for the project:

1. Caffe integration and real image classification.
2. Object localization on real images using object proposals.
3. Support for training/fine tuning network using caffe.
4. Integration with Robocomp simulation environment and support for CAD models. 
5. Regress testing for both components.
6. Use cases / samples and documentation for both cases.
7. CAD models dataset with classification and detection support for each of them.

----------------
Harit Pandya
