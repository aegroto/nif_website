+++
title = "Conclusion"
weight = 8
[extra]
align = "justify"
+++

We have proposed NIF, a novel image compression method based on INRs which quantitatively and qualitatively outperforms current INR-based methods. In addition, the proposed approach drastically improves the computational requirements with a speed-up of x26 for some configurations, while preserving image quality. Visual comparisons show that the decompressed images are less noisy with respect to previous INR-based methods and do not suffer from well-known distortions such as blocking artifacts, which are instead common in traditional approaches.
Likewise standard codecs, the [reference encoder](https://github.com/aegroto/nif) produces stand-alone compressed files packed with metadata that can be decompressed using a compliant decoder.
In future works, we plan to put efforts into improving the reconstruction capabilities and speed of these methods, along with exploring their efficiency in multiple use cases.
