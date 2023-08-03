+++
title = "Abstract"
[extra]
align = "justify"
+++

In Implicit Neural Representations (INRs) a discrete signal is parameterized by a neural network that maps coordinates to the signal samples. 
INRs were successfully employed for encoding and compression, but such approaches are in their early stage and are still overcome by traditional codecs and autoencoders. Despite this, they have recently gained the attention of the research community due to their promising results as novel representation strategies for encoding visual content.
In this paper, we propose Neural Imaging Format (NIF), an open-source INR-based image compression codec which takes advantage of a novel neural architecture which consists of two modules: a Genesis network, for mapping coordinates to pixels through bottleneck layers with sinusoidal activation units, and a Modulation network, for varying the period of the sinusoidal activations. Additionally, a final weights quantization step leads to an improvement in the compression ratio.
Our proposal (NIF) consistently outperforms state-of-art INR-based compressors in terms of PSNR, by achieving comparable or better results with an outstanding up to x26 encoding speed. We also show that NIF reduces the gap between INR-based methods with respect to traditional approaches. Interestingly, our approach outperforms established codecs such as JPEG and WebP when one encodes high-resolution images at low-bitrate regimes. Extensive experiments on different datasets, a visual comparison, and an ablation study, prove the validity of the proposed approach.


