# Image-generation-step-by-step-animation-generation-image-translation

[![Watch the video](https://github.com/Happypiepie/Image-generation-step-by-step-animation-generation-image-translation/blob/main/2021_05_05_15_05_15.gif)](https://github.com/Happypiepie/Image-generation-step-by-step-animation-generation-image-translation/blob/main/2021_05_05_15_05_15.gif)

# Abstract
Generative adversarial networks play an important role in image generation, but the successful generation of high-resolution
images from complex data sets remains a challenging goal. In this paper, we propose the LGAN (Link Generative Adversarial
Networks) model, which can effectively enhance the quality of the synthesized images. The LGAN model consists of two
parts, G1 and G2. G1 is responsible for the unconditional generation part, which generates anime images with highly abstract
features containing few coefficients but continuous image elements covering the overall image features. Moreover, G2 is
responsible for the conditional generation part (image translation), consisting of mapping and Superresolution networks. The
mapping network fills the output of G1 into the real-world image after semantic segmentation or edge detection processing;
the Superresolution network super-resolves the actual picture after completing mapping to improve the image’s resolution.
In the comparison test with WGAN, SAGAN, WGAN-GP and PG-GAN, this paper’s LGAN(SEG) leads 64.36 and 12.28,
respectively, fully proving the model’s superiority.
![This is an image](https://github.com/Happypiepie/Image-generation-step-by-step-animation-generation-image-translation/blob/main/FIG4.png)
![This is an image](https://github.com/Happypiepie/Image-generation-step-by-step-animation-generation-image-translation/blob/main/FIG4.png)

# Requirements

 * Python 3.6, PyTorch >= 1.6
 
 * Requirements: opencv-python, tqdm
 
 * Platforms: Ubuntu 16.04, cuda-10.0 & cuDNN v-7.5

# Datasets
 
### Train、Val Dataset
The train and val datasets are sampled from Dvind-2017. Train dataset has 16700 images and Val dataset has 425 images. Download the datasets from here, and then extract it into data directory. Finally run
 
```
python data_processpy

optional arguments:
--upscale_factor      super resolution upscale factor [default value is 3]
```
 
# Train
 
```
python train.py

optional arguments:
--upscale_factor       upscale factor [default value is 3]
--is_real_time         real time to show [default value is False]
--delay_time           delay time to show [default value is 1]
--model_name           model name [default value is epoch_3_100.pt]
```
 
 
## Running the tests
 
 
```
python test.py

```

The result in results folder.
 
# Benchmarks
Adam optimizer were used with learning rate scheduling between epoch 30 and epoch 80.

Upscale Factor = 2

Epochs with batch size of 64 takes ~1 minute on a NVIDIA GeForce 3090 GPU.



# Cite
 
 
```
@article{jing2021video,
  title={Video prediction: a step-by-step improvement of a video synthesis network},
  author={Jing, Beibei and Ding, Hongwei and Yang, Zhijun and Li, Bo and Bao, Liyong},
  journal={Applied Intelligence},
  pages={1--13},
  year={2021},
  publisher={Springer}
}

```










 

