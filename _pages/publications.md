---
permalink: /publications/
title: "Behind the Pixels"
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/Header1.jpg
  caption: 'Rendered with EDXRay'
excerpt: ''
---

---

### ExtraNet: Real-time Extrapolated Rendering for Low-latency Temporal Supersampling

**Jie Guo, Xihao Fu, Liqiang Lin, Hengjun Ma, Yanwen Guo, Shiqiu (Edward) Liu, Ling-Qi Yan**

_ACM Transactions on Graphics (Proceedings of SIGGRAPH Asia 2021)_

![](/assets/images/pages/extra_teaser.png){: .align-left width="400px" }

Both the frame rate and the latency are crucial to the performance of real-time rendering applications such as video games. Spatial supersampling methods, such as the Deep Learning SuperSampling (DLSS), have been proven successful at decreasing the rendering time of each frame by rendering at a lower resolution. But temporal supersampling methods that directly aim at producing more frames on the fly are still not practically available. This is mainly due to both its own computational cost and the latency introduced by interpolating frames from the future. In this paper, we present ExtraNet, an efficient neural network that predicts accurate shading results on an extrapolated frame, to minimize both the performance overhead and the latency. With the help of the rendered auxiliary geometry buffers of the extrapolated frame, and the temporally reliable motion vectors, we train our ExtraNet to perform two tasks simultaneously: irradiance in-painting for regions that cannot find historical correspondences, and accurate ghosting-free shading prediction for regions where temporal information is available. We present a robust hole-marking strategy to automate the classification of these tasks, as well as the data generation from a series of high-quality production-ready scenes. Finally, we use lightweight gated convolutions to enable fast inference. As a result, our ExtraNet is able to produce plausibly extrapolated frames without easily noticeable artifacts, delivering a 1.5 to near 2 increase in frame rates with minimized latency in practice.


[Paper](https://sites.cs.ucsb.edu/~lingqi/publications/paper_extranet.pdf)

### ReSTIR GI: Path Resampling for Real-Time Path Tracing

**Yaobin Ouyang, Shiqiu Liu, Markus Kettunen, Matt Pharr, Jacopo Pantaleoni**

_Computer Graphics Forum (Proceedings of High Performance Graphics 2021)_

![](/assets/images/pages/ReSTIR-GI-Teaser.png){: .align-left width="400px" }

Even with the advent of hardware-accelerated ray tracing in modern GPUs, only a small number of rays can be traced at each pixel in real-time applications. This presents a significant challenge for path tracing, even when augmented with state-of-the art denoising algorithms. While the recently-developed ReSTIR algorithm [Bitterli et al. 2020] enables high-quality renderings of scenes with millions of light sources using just a few shadow rays at each pixel, there remains a need for effective algorithms to sample indirect illumination.

We introduce an effective path sampling algorithm for indirect lighting that is suitable to highly parallel GPU architectures. Building on the screen-space spatio-temporal resampling principles of ReSTIR, our approach resamples multi-bounce indirect lighting paths obtained by path tracing. Doing so allows sharing information about important paths that contribute to lighting both across time and pixels in the image. The resulting algorithm achieves a substantial error reduction compared to path tracing: at a single sample per pixel every frame, our algorithm achieves MSE improvements ranging from 9.3x to 166x in our test scenes. In conjunction with a denoiser, it leads to high-quality path traced global illumination at real-time frame rates on modern GPUs

[Paper](https://d1qx31qr3h6wln.cloudfront.net/publications/ReSTIR%20GI.pdf)

### Temporally Reliable Motion Vectors for Real-time Ray Tracing

**Zheng Zeng, Shiqiu (Edward) Liu, Jinglei Yang, Lu Wang, Ling-Qi Yan**

_Computer Graphics Forum (Proceedings of Eurographics 2021)_

![](/assets/images/pages/mvec.png){: .align-left width="360px" }

Real-time ray tracing (RTRT) is being pervasively applied. The key to RTRT is a reliable denoising scheme that reconstructs clean images from significantly undersampled noisy inputs, usually at 1 sample per pixel as limited by current hardware’s computing power. The state of the art reconstruction methods all rely on temporal filtering to find correspondences of current pixels in the previous frame, described using per-pixel screen-space motion vectors. While these approaches are demonstrated powerful, they suffer from a common issue that the temporal information cannot be used when the motion vectors are not valid, i.e. when temporal correspondences are not obviously available or do not exist in theory. We introduce temporally reliable motion vectors that aim at deeper exploration of temporal coherence, especially for the generally-believed difficult applications on shadows, glossy reflections and occlusions, with the key idea to detect and track the cause of each effect. We show that our temporally reliable motion vectors produce significantly better temporal results on a variety of dynamic scenes when compared to the state of the art methods, but with negligible performance overhead.

[Paper](https://sites.cs.ucsb.edu/~lingqi/publications/paper_trmv.pdf), [Video](https://sites.cs.ucsb.edu/~lingqi/publications/video_trmv.mp4)

### Neural FFTs for Universal Texture Image Synthesis

**Morteza Mardani, Guilin Liu, Aysegul Dundar, Shiqiu Liu, Andrew Tao, Bryan Catanzaro**

_Advances in Neural Information Processing Systems 33 (NeurIPS 2020)_

![](/assets/images/pages/fft.png){: .align-left width="460px" }

Synthesizing larger texture images from a smaller exemplar is an important task in graphics and vision. The conventional CNNs, recently adopted for synthesis, require to train and test on the same set of images and fail to generalize to unseen images. This is mainly because those CNNs fully rely on convolutional and upsampling layers that operate locally and not suitable for a task as global as texture synthesis. In this work, inspired by the repetitive nature of texture patterns, we find that texture synthesis can be viewed as (local) \textit{upsampling} in the Fast Fourier Transform (FFT) domain. However, FFT of natural images exhibits high dynamic range and lacks local correlations. Therefore, to train CNNs we design a framework to perform FFT upsampling in feature space using deformable convolutions. Such design allows our framework to generalize to unseen images, and synthesize textures in a single pass. Extensive evaluations confirm that our method achieves state-of-the-art performance both quantitatively and qualitatively.

[Paper](https://proceedings.neurips.cc/paper/2020/file/a23156abfd4a114c35b930b836064e8b-Paper.pdf)

### Transposer: Universal Texture Synthesis Using Feature Maps as Transposed Convolution Filter

**Guilin Liu, Rohan Taori, Ting-Chun Wang, Zhiding Yu, Shiqiu Liu, Fitsum A. Reda, Karan Sapra, Andrew Tao, Bryan Catanzaro**

![](/assets/images/pages/transposer.jpg){: .align-left width="360px" }

Existing texture synthesis usually suffers from several issues: non-learning based approaches, which mainly rely on iterative optimization, are usually very slow; recent deep learning-based approaches usually over-fit to a single texture image or a fixed set of texture images and therefore can't generalize to new unseen texture images. In this work, we present a deep learning framework that can do texture synthesis for arbitrary input texture image with output texture larger than the input in near real-time. Our framework is built on transpose convolution operation where the transpose convolution filters are the encoded features of the input texture and the transpose convolution inputs are the features' self-similarity maps. Visual and quantitative comparisons show that our method significantly out-performs prior methods while being hundreds of times faster.  

[Preprint](https://arxiv.org/pdf/2007.07243.pdf), [Video](https://www.youtube.com/watch?v=8Us9c5iBRCY)

### A Survey of Temporal Antialiasing Techniques

**Lei Yang, Shiqiu Liu, Marco Salvi**

_Eurographics 2020, State of the Art Report_

![](/assets/images/pages/TAA.jpg){: .align-left width="600px" }
Temporal Antialiasing (TAA), formally defined as temporally-amortized supersampling, is the most widely used antialiasing technique in today’s real-time renderers and game engines. This survey provides a systematic overview of this technique. We first review the history of TAA, its development path and related work. We then identify the two main sub-components of TAA, sample accumulation and history validation, and discuss algorithmic and implementation options. As temporal upsampling is becoming increasingly relevant to today’s game engines, we propose an extension of our TAA formulation to cover a variety of temporal upsampling techniques. Despite the popularity of TAA, there are still significant unresolved technical challenges that affect image quality in many scenarios. We provide an in-depth analysis of these challenges, and review existing techniques for improvements. Finally, we summarize popular algorithms and topics that are closely related to TAA. We believe the rapid advances in those areas may either benefit from or feedback into TAA research and development.

[Preprint](/assets/files/TemporalAA.pdf)

---

### Cinematic Rendering in UE4 with Real-Time Ray Tracing and Denoising

**Edward Liu, Ignacio Llamas, Juan Cañada, Patrick Kelly**

_Ray Tracing Gems_

![](/assets/images/pages/Reflections.jpg){: .align-left width="360px" }
We present cinematic quality real-time rendering by integrating ray tracing in Unreal Engine 4. We improve the state-of-the-art performance in GPU ray tracing by an order of magnitude through a combination of engineering work, new ray tracing hardware, hybrid rendering techniques, and novel denoising algorithms.


[Pdf](https://link.springer.com/content/pdf/10.1007%2F978-1-4842-4427-2_19.pdf)

---

### Spatiotemporal Variance-Guided Filtering: Real-Time Reconstruction for Path-Traced Global Illumination

**Christoph Schied, Anton Kaplanyan, Chris Wyman, Anjul Patney, Chakravarty R. Alla Chaitanya, John Burgess, Shiqiu Liu, Carsten Dachsbacher, Aaron Lefohn, Marco Salvi**

_High Performance Graphics 2017 (Best Paper Award)_

![](/assets/images/pages/SVGF.jpg){: .align-left width="600px" }
We introduce a reconstruction algorithm that generates a temporally stable sequence of images from one path-per-pixel global illumination. To handle such noisy input, we use temporal accumulation to increase the effective sample count and spatiotemporal luminance variance estimates to drive a hierarchical, image-space wavelet filter [Dammertz et al. 2010]. This hierarchy allows us to distinguish between noise and detail at multiple scales using local luminance variance.
Physically based light transport is a long-standing goal for realtime computer graphics. While modern games use limited forms of ray tracing, physically based Monte Carlo global illumination does not meet their 30 Hz minimal performance requirement. Looking ahead to fully dynamic real-time path tracing, we expect this to only be feasible using a small number of paths per pixel. As such, image reconstruction using low sample counts is key to bringing path tracing to real-time. When compared to prior interactive reconstruction filters, our work gives approximately 10× more temporally stable results, matches reference images 5–47% better (according to SSIM), and runs in just 10 ms (± 15%) on modern graphics hardware at 1920×1080 resolution.

[Preprint](/assets/files/hpg17_svgf.pdf)

---

### Computer Simulations Imply Forelimb-Dominated Underwater Flight in Plesiosaurs

**Shiqiu Liu, Adam S. Smith, Yuting Gu, Jie Tan, C. Karen Liu and Greg Turk**

_PLoS Computational Biology_

![](/assets/images/pages/Underwater Plesiosaur High Res.jpg){: .align-left width="400px" }

Plesiosaurians are an extinct group of highly derived Mesozoic marine reptiles with a global distribution that spans 135 million years from the Early Jurassic to the Late Cretaceous. During their long evolutionary history they maintained a unique body plan with two pairs of large wing-like flippers, but their locomotion has been a topic of debate for almost 200 years. Key areas of controversy have concerned the most efficient biologically possible limb stroke, i.e whether it consisted of rowing, underwater flight, or modified underwater flight; and how the four limbs moved in relation to each other: did they move in or out of phase? Previous studies have investigated plesiosaur swimming using a variety of methods, including skeletal analysis, human swimmers, and robotics. We adopt a novel approach using a digital, three-dimensional, articulated, free-swimming plesiosaur in a simulated fluid. We generated a large number of simulations under various joint degrees of freedom to investigate how the locomotory repertoire changes under different parameters. Within the biologically possible range of limb motion, the simulated plesiosaur swims primarily with its forelimbs using an unmodified underwater flight stroke, essentially the same as turtles and penguins. In contrast, the hindlimbs provide relatively weak thrust in all simulations. We conclude that plesiosaurs were forelimb-dominated swimmers that used their hind limbs mainly for maneuverability and stability.

Full paper at [PLoS Computational Biology](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004605).

Press Coverage:

1. [What Looks Like a Dinosaur But Swims Like a Penguin? It’s the Meyerasaurus.](http://www.usatoday.com/story/news/2015/12/17/meyerasaurus-dinosaur-swam-like-penguin/77507996/) _USA Today, 12/18/2015_
2. [Ancient Marine Reptiles Flew through the Water](http://www.livescience.com/53150-swimming-plesiosaurs.html) _Live Science, 12/18/2015_
3. [Plesiosaurs Literally Flew through Ocean](http://www.seeker.com/plesiosaurs-literally-flew-through-oceans-1770627747.html) _Discovery News, 12/17/2015_