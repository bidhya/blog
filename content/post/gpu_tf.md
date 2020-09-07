---
title: "GPU installation on Windows 10 for Tensorflow"
date: 2020-09-06
---

Even though Tensorflow installation is straighforward now with pip (even on Windows), there are still few nuances on using GPU. Here I describe the steps to install various drivers to make Tensorflow run on GPU. Refere to this [page](https://www.tensorflow.org/install/gpu)for specific GPU version of sofware/driver  
**Important** : Make sure to download the exact version specified on google site. Since, there is rapid updates to both tensorflow and nvidia, downloading the latest NVIDIA drivers will NOT work with Tensorflow.  

The following NVIDIA® Software and Drivers must be installed:  
1. NVIDIA® GPU drivers —CUDA® 10.1 requires 418.x or higher.  
    Choose the GPU driver matching your GPU, search, download, and install  
2. CUDA® Toolkit —TensorFlow supports CUDA® 10.1 (TensorFlow >= 2.1.0)
    Search, download, and install (size > 2 GB)
3. CUPTI ships with the CUDA® Toolkit: This should already be installed with cuda toolkit installation  
4. cuDNN SDK 7.6
    Need to make an account, login, then download and unzip to folder (C:/tools/)  
5. (Optional) TensorRT 6.0 to improve latency and throughput for inference on some models.  
    Download and unzip to same folder (C:/tools/)  

### Set paths with environment variables [either user or system will work, but I prefer system path]
- C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\bin  
- C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\extras\CUPTI\lib64  
- C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\include  
- C:\tools\cuda\bin  
- C:\tools\TensorRT-6.0.1.5 (optional)  

