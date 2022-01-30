# Navigation Project
# Udaicity Nanodegree - Deep Reinforcement Learning

## Introduction

The Navigation project solves a simple environment where the task of the agent is to collect yellow bananas and avoid blue ones. The challenge is defined by the following parameters:

### Rewards
`-1` for blue bananas
`+1` for yellow bananas

### Actions 
`0` move forward
`1` move backward
`2` turn left
`3` turn right

### State
defined by a 37 dimensional vector

### Goal
Average score of +13
under 1800 training episodes

## Requirements
The requiremnts needed for the project are listed below.
```
unityagents
numpy
torch
matplotlib (for plotting the learning curve)
```

These libraries are also listed in the `requiremnts.txt` with the used version numbers.

## Setup Guide
This projects first requires the download and setup of the project environment. This depends on the operating system:

 - [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
 - [Mac OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
 - [Windows (32-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
 - [Windows (64-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

The path to the downloaded files should be modified in the first code cell of the `Navigation.ipnb` notebook.

The code for starting the learning process can be found in the `Navigation.ipnb`. For setup the `python` folder from the course excercise is needed in the same directory