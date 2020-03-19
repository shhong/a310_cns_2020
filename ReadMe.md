# A310 Computational Neuroscience - Okinawa Institute of Science and Technology, 2019/2020
This repository contains modeling practice materials and homework for the Computational Neuroscience course at Okinawa Institute of Science and Technology in 2020. Our modeling exercise classes are basically about exploring physiological concepts about how neural systems function via computer simulations. The goal is to learn how computational models can help us understand how diverse phenomena in real neural systems arise from the underlying physical principles.

We will mainly use the [NEURON](https://www.neuron.yale.edu/neuron/) simulation platform, which uses [Python](https://www.python.org) programming language for the interface. We will also cover some basic analysis techniques for neural data, while most of our focus will be constructing models and running their simulations.


## Software
We will use [NEURON](https://www.neuron.yale.edu/neuron/) 7.7.2 with Python 3.7. **We recommend using our Docker container**, since NEURON is quite challenging for first-time users to configure correctly. **See the [installation guide](./docker/ReadMe.md) for how to install and use the Docker and container**. If you do not want to use this, we recommend compiling the source by following the [instruction](https://www.neuron.yale.edu/neuron/download/getstd) carefully. We discourage installation via binary installers, which has been a source of frustration in the past.


## Schedule of modeling classes and homework dues

### [Modeling class introduction](https://github.com/shhong/a310_cns_2020/tree/master/class_intro) — Jan 20, 2020

In this intro class, we will cover some basics of Python programming language and model building in NEURON.

### [Modeling class 1](https://github.com/shhong/a310_cns_2020/tree/master/class_1) — Feb 6, 2020

In our first class, we will learn how to do virtual current clamp experiments in NEURON.

### [Modeling class 2](https://github.com/shhong/a310_cns_2020/tree/master/class_2) — Feb 13, 2020

In the second class, we will learn how  to connect external inputs to synapses in a neuron, making the first network simulation.

### [Modeling class 3](https://github.com/shhong/a310_cns_2020/tree/master/class_3) - Mar 19, 2020

In the third class, we will learn about how to make and use custom cellular mechanisms and also more about building network models.

### Modeling class 4 - Apr 9, 2020

In the last class, we will discuss more about building neural network models and adding synaptic plasticity.


### [*Homework 1](https://github.com/shhong/a310_cns_2020/tree/master/homework_1/Homework%201.ipynb) — Due: Feb 26, 2020

### [*Homework 2](https://github.com/shhong/a310_cns_2020/blob/master/homework_2/Homework%202.ipynb) - Due: Mar 27, 2020


---
_Written by Sungho Hong, Computational Neuroscience Unit, Okinawa Institutes of Science and Technology_

_January 2020
