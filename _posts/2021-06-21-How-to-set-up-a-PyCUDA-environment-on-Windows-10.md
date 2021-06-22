---
layout: post
title: How to set up a PyCUDA environment on Windows 10
date: 2021-06-21
published: true
categories: tutorials
image:
---
<h1>How to set up a PyCUDA environment on Windows 10<h1/>
<p>
<h5>Firstly, the following programs need to be downloaded and installed:</h5>
</p>
<p>
- Anaconda 3 (with Latest Python) -- https://www.anaconda.com/products/individual#Downloads
</p>
<p>
- Visual Studio 2019 -- https://visualstudio.microsoft.com/downloads/
</p>
<p>
- CUDA Toolkit 11.2 -- https://developer.nvidia.com/cuda-11.2.0-download-archive
</p>
<p>
- CUDA Toolkit 11.3 -- https://developer.nvidia.com/cuda-downloads
</p>
<p>
The Visual Studio download will prompt you to install packages for its environment, select the relevant data science packages and the C++ integration on the menu on the right hand side.

The others just require the default settings.
</p>
<p>
<h5>Once these are all downloaded and installed, create a batch file labeled "launch-python-cuda-environment.bat" with the following contents:</h5>
</p>
<p>

<p>
call "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Auxiliary\Build\vcvarsall.bat" x64
</p>
<p>
call "C:\Users\your_name\Anaconda3\Scripts\activate.bat" C:\Users\your_name\Anaconda3
</p>
<p>
cmd
</p>
</p>
<p>
It is important to note that:
</p>
<p>
1. The first line of your batch file needs to point to the vcvarsall.bat file in your Visual Studio installation (May be in a different location than described above).
</p>
2. CUDA toolkits need to be added to the path variable for your command prompt.
<p>
3. The second line needs to point to your activate.bat file which also might be in a different location in your installation.
</p>
<p>
Run your launch-python-cuda-environment.bat file and a command prompt will open with the PyCUDA environment.

Use the DeviceQuery.py file to test that your PyCUDA environment is running properly and that your GPU is CUDA-enabled.
</p>
