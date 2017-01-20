---
permalink: /projects/
title: "Behind the Pixels"
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/Header1.jpg
  caption: 'Rendered with EDXRay'
excerpt: 'Focus on Computer Graphics and Computer Vision.'
---

---

### EDXRay

EDXRay is a physically based render independently developed by [Edward Liu](http://behindthepixels.info/). It is built with modern C++. Aside from many low level optimizations, parallelism is exploited on both thread level and instruction level so it's highly performant. It includes many state of the art algorithms published in recent years in light transport simulation, material modelling, sampling and reconstruction, camera models as well as participating media.

Please visit [behindthepixels.info/EDXRay/](http://behindthepixels.info/EDXRay/) for more detailed introduction.

---

### EDXRaster

EDXRaster is an highly optimized software renderer based on rasterization, independently developed by [Edward Liu](http://behindthepixels.info/). This renderer is written with C++ and SSE and is highly optimized. Most of the D3D11 pipeline is implemented.

Please visit [behindthepixels.info/EDXRaster/](http://behindthepixels.info/EDXRaster/) for more detailed introduction.

---

### EDXFluids

EDXFluids is a fully featured fluid simulator independently developed by [Edward Liu](http://behindthepixels.info/). It's built with C++ with multithreading support. EDXFluids heavily uses template in all of its data containers and algorithms so it can easily instantiate simulators of different dimensions. Development process is tremendously benefited from this since it is really simple to debug and visualize new algorithms in 2 dimensional simulations before trivially changing it to 3 dimensional. Currently, the simulator is capable of simulating smoke and liquid as well as their interaction with static solid objects.

Please visit [behindthepixels.info/EDXFluids/](http://behindthepixels.info/EDXFluids/) for more detailed introduction.