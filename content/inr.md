+++
title = "Introduction to Implicit Neural Representations (INRs)"
weight = 3
[extra]
align = "justify"
+++


Implicit Neural Representation (INR) is a very recent paradigm for data encoding, where a data point is reinterpreted as a map from coordinates to some features.
This mapping is then approximated by a neural network, which is purposely trained to overfit the task, resulting in a continuous functional representation of the data point. This concept is the foundation for a variety of works that propose multiple techniques to derive functional representations of various data types such as 3D shapes, radiance fields, videos and images.

Neural Image Format (NIF), the INR-based compression approach we propose, relies on training a representational network that maps input coordinates to pixels.
The network parameters are then quantized and compressed to minimize the size of encoded data.
These methods are penalized by the computational cost to overfit a neural network on the signal and by the time required to obtain a compressed representation.
Our proposal leverages various tweaks to aid the network during training and to reduce the time needed to obtain an optimal approximation of the target signal.
