+++
title = "Quantitative results"
weight = 7
[extra]
align = "justify"
+++

## INR-based image compression
Our proposal NIF outperforms previous works on the field in terms of PSNR on Kodak while achieving comparable performance on CelebA.

{{ figure(path="plots/inr_all.svg") }}

It is fair to point out that Strumpler et al. approach achieves comparable or better PSNR when using meta-learned initializations on CelebA; this is not surprising since the base parameters are learned on the same CelebA dataset, which is characterized by a limited images variability, and therefore allows the network to leverage the consistent redundancies that are typically absent in real scenarios.

{% vc_slider() %}
{{ vc(img_id="celeba_189985", kind="celeba") }}
{% end %}

*In this CelebA picture, NIF reconstruction is notably less noisy than Strumpler's. 
Although WebP is able to capture some finer details it suffers from evident block artifacts while INR-based methods do not.*


## Comparison to traditional approaches

### *Kodak*
On this dataset, our proposal NIF clearly outperforms JPEG and performs comparably to modern codecs, such as BPG and WebP, in terms of PSNR at low bitrates.
In terms of MS-SSIM, NIF performs similarly to JPEG2000. 

{{ figure(path="plots/traditional_kodak.svg") }}

These results clearly reduce the gap between INR-based compression and classical methods with respect to the previous baseline given by the basic version of Strumpler et al., which is reported in the plot for reference. 

{% vc_slider() %}
{{ vc(img_id="kodak_8", kind="kodak") }}
{% end %}

*Although state-of-the-art methods, such as BPG and Xie et al. approach, achieve asmoother reconstruction, it is noticeable that they tend to remove a lot of small details, reconstructing some patches as uniform colour blocks. 
This is clear on the Kodak picture #8.
In contrast, both NIF and Strumpler basic reconstruct this grainy structure, but NIF better encodes uniform patches.*

### *Image Compression Benchmark (ICB)*

On the high-resolution images ICB dataset our proposal NIF outperforms some baselines in terms of PSNR at low bitrates (0.08bpp), with a PSNR gain of +0.41dB compared with the modern WebP codec and a gain of +3.07dB against JPEG. 
Concerning higher bitrates (0.22bpp), the results of NIF are comparable to WebP and JPEG, but they are still outperformed by BPG. 
These promising results suggest that INR-based methods could be used as an effective tool to compress high-resolution images.


{{ figure(path="plots/traditional_icb.svg") }}
