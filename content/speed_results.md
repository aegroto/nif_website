+++
title = "Compression speed improvements"
weight = 6
[extra]
align = "justify"
+++

The following results show that our method achieves comparable or better results compared to COIN and the basic version of Strumpler et al. with much lower compression times.
We select configurations that achieve similar bits-per-pixel at full resolution and report the average PSNR and SSIM as reference.
The advantage is evident, especially at lower bitrates, for instance when using an average of 0.3 bits-per-pixel to encode x2 downsampled pictures NIF has about x26 compression speed (65 minutes vs 1685 minutes) and a slightly lower SSIM than Strumpler basic (0.891 vs 0.920):

{{ speed_table(case_id="x2_033bpp") }}

At 1.0 bits-per-pixels and x4 downsampled images, our proposal NIF achieves the best results in terms of PSNR and SSIM with a large time saving (x10). It is important to note that the running time of NIF is quite similar for all the four configurations we investigated, while COIN and Strumpler basic's running time drastically goes up when the image resolution increases.

{{ speed_table(case_id="x4_1bpp") }}
