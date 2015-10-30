---
layout: post
title: YAML parsing in C++ using yaml-cpp
---


In this post I want to discuss how I will use yaml-cpp for parsing a YAML document.
The document I intend to parse contains description about what I call "command 
primitives" for PANDUbot. Command primitives are atomic commands that the robot
controller's executive layer can directly execute. For example a complex command
like "Goto vending machine and Get snickers" has two command primitives: "Goto"
and "Get" that are connected by the word "and". The thing following the command
primitive defines the goal of the robot for that particular command primitive. 
The YAML file I am parsing will actually contain a list of the command primitives
PANDUbot can recognize and the recognized goals.
