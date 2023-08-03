+++
title = "Network architecture"
weight = 5
[extra]
align = "justify"
+++

{{ side_figure(path="figures/architecture.svg") }}


The architecture consists of two modules, named Genesis network and Modulation network.
The genesis network is a multi-layer representational perceptron with sinusoidal activations ([SIREN](https://www.vincentsitzmann.com/siren/)) responsible for calculating features of a pixel when fed with its coordinates. In contrast to traditional SIRENs, the period of each sinusoidal activation is altered based on the period variation provided by the Modulation network, a dedicated module that adjusts the hidden feature period, thereby adapting to variations in frequency across different regions of the image.


