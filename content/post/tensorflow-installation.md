---
title: Install Tensorflow with Anaconda
summary: Read about how to install Tensorflow within Anaconda environment.
description: Read about how to install Tensorflow within Anaconda environment.
categories: [Machine Learning]
tags: [Anaconda, Tensorflow, Installation]
date: 2018-02-18
weight: 1
draft: false
searchHidden: false
cover:
  image: "" # image path/url
  caption: "" # display caption under cover
  alt: "" # alt text
  relative: true # when using page bundles set this to true
---

1. Go to https://www.anaconda.com/download to download anaconda  
2. Open terminal and change directoray to where anaconda.sh is, then bash it.  
``` bash {linenos=true}
bash Anaconda3-5.1.0-Linux-x86_64.sh
```
3. Build anaconda environment named tensorflow
``` bash {linenos=true}
conda create --name tensorflow python=3
```
4. Active tensorflow environment
```bash {linenos=true}
source activate tensorflow
```
5. Install tensorflow
```bash {linenos=true}
pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.5.0-cp36-cp36m-linux_x86_64.whl
```
6. To open `anaconda-navigator`
7. Install jupyter notebook in home window
8. Import `environment-cpu.yml` to Anaconda
``` yaml {linenos=true}
name: tf-cpu
channels:
    - https://conda.anaconda.org/menpo
    - conda-forge
dependencies:
    - python==3.5.2
    - numpy
    - matplotlib
    - jupyter
    - opencv3
    - pillow
    - scikit-learn
    - scikit-image
    - scipy
    - h5py
    - eventlet
    - flask-socketio
    - seaborn
    - pandas
    - ffmpeg
    - imageio=2.1.2
    - pyqt=4.11.4
    - pip:
        - moviepy
        - tensorflow==1.4.0
        - keras==2.0.8
```
9. Hit Environments in left column, run tf-cpu with jupyter notebook
