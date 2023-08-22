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

{{ vc(img_id="celeba_189985", kind="celeba") }}

***
*In this CelebA picture, NIF reconstruction is notably less noisy than Strumpler's. 
Although WebP is able to capture some finer details it suffers from evident block artifacts while INR-based methods do not.*
***

## Comparison to traditional approaches

### *Kodak*
On this dataset, our proposal NIF clearly outperforms JPEG and performs comparably to modern codecs, such as BPG and WebP, in terms of PSNR at low bitrates.
In terms of MS-SSIM, NIF performs similarly to JPEG2000. 

{{ figure(path="plots/traditional_kodak.svg") }}

These results clearly reduce the gap between INR-based compression and classical methods with respect to the previous baseline given by the basic version of Strumpler et al., which is reported in the plot for reference. 

{{ vc(img_id="kodak_8", kind="kodak") }}

***
*Although state-of-the-art methods, such as BPG and Xie et al. approach, achieve a smoother reconstruction, it is noticeable that they tend to remove a lot of small details, reconstructing some patches as uniform colour blocks. 
This is clear on the Kodak picture #8.
In contrast, both NIF and Strumpler basic reconstruct this grainy structure, but NIF better encodes uniform patches.*
***

### *Image Compression Benchmark (ICB)*

On the high-resolution images ICB dataset our proposal NIF outperforms some baselines in terms of PSNR at low bitrates (0.08bpp), with a PSNR gain of +0.41dB compared with the modern WebP codec and a gain of +3.07dB against JPEG. 
Concerning higher bitrates (0.22bpp), the results of NIF are comparable to WebP and JPEG, but they are still outperformed by BPG. 

{{ figure(path="plots/traditional_icb.svg") }}

{{ vc(img_id="icb_deer", kind="icb") }}

{{ vc(img_id="icb_flower_foveon", kind="icb") }}

***
*On these crops, NIF obtains similar visual results. 
In particular, in flower foveon, NIF reconstruction presents fewer blocking artifacts, which we believe is a strong positive factor of INR-based methods with respect to traditional ones. 
In deer, NIF tends to reconstruct grainy noise in the background while classical codecs remove these details.*
***

These promising results suggest that INR-based methods could be used as an effective tool to compress high-resolution images.
