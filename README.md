# WiT Network

<a href="https://ieeexplore.ieee.org/document/10246273"> </a>

This is the implementation code for the paper *titled:* [Restoring Snow-Degraded Single Images With Wavelet in Vision Transformer](https://ieeexplore.ieee.org/document/10246273), IEEE Access 2023.

<p align="left">
  <img src="imgs/architecture.png" width="800"/>
</p>

# Executive Summary:

Images corrupted by snowy adverse weather can impose performance impediments to critical high-level vision-based applications. Restoring snow-degraded images is vital, but the task is ill-posed and very challenging due to the veiling effect, stochastic distribution, and multi-scale characteristics of snow in a scene. In this regard, many existing image denoising methods are often less successful with respect to snow removal, being that they mostly achieve success with one snow dataset and underperform in others, thus questioning their robustness in tackling real-world complex snowfall scenarios. In this paper, we propose the wavelet in transformer (WiT) network to address the image desnow inverse problem. Our model exploits the joint systemic capabilities of the vision transformer and the renowned discrete wavelet transform to achieve effective restoration of snow-degraded images. In our experiments, we evaluated the performance of our model on the popular SRRS, SNOW100K, and CSD datasets, respectively. The efficacy of our learning-based network is proven by our obtained numeric and qualitative result outcomes indicating significant performance gains compared to image desnow benchmark models and other state-of-the-art methods in the literature.

# How to Run the Code:

- Recommended Python versions is from 3.7 to 3.8, and CUDA versions 10.2 to 11.5

- Download or Clone this repository

```
git clone https://github.com/WINS-lab/WiT
cd WiT
```

- Install package dependencies `pip3 install -r requirements.txt`

- PyTorch environment with GPU support for Windows and Linux can be installed with Conda `conda install pytorch==1.7.1 torchvision==0.8.2 torchaudio==0.7.2 cudatoolkit=10.2 -c pytorch`

## Data format

- Create a `data` folder and format the test dataset snow-degraded input and gt images as follows

```
    WiT
    |
    ├── data
    |   | 
    |   ├── test  # Test-set         
    |   |   ├── <dataset_name>          
    |   |   |   ├── input         # degraded images 
    |   |   |   └── gt            # clean images
    |   |   └── dataset_filename.txt
```

# Datasets:

The underlisted snow-image datasets were used for the evaluation of the WiT network
- SNOW100K-L [download link](https://sites.google.com/view/yunfuliu/desnownet)
- SRRS [download link](https://ntucc365-my.sharepoint.com/personal/f05943089_ntu_edu_tw/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ff05943089%5Fntu%5Fedu%5Ftw%2FDocuments%2FSRRS%2Ezip&parent=%2Fpersonal%2Ff05943089%5Fntu%5Fedu%5Ftw%2FDocuments&ga=1)
- CSD [download link](https://drive.google.com/file/d/1smNrDvtPs89e0xk336Rt2-2KZffyX5H-/view)

# Acknowledgement
Useful blocks of code adapted in the WiT is credited to the contributions of [ImageNetModel](https://github.com/yehli/imagenetmodel), [TransWeather](https://github.com/jeya-maria-jose/TransWeather/), and [ViT-PyTorch](https://github.com/lucidrains/vit-pytorch) 
