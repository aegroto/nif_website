+++
title = "Training process"
weight = 4
[extra]
align = "justify"
+++

![Flow](processing_flow.svg)
The training of a neural network typically consists of executing a number of epochs, each containing several iterations. 
However, many state-of-the-art implicit image compression approaches lack a clear subdivision of the overall training process. 
Our approach leverages a step-wise decomposition of both the fitting and quantization fine-tuning processes, as it enables one to perform some optimisations on the network at specific stages, such as weights restart.
