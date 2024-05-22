---
title: Image to Image (Basic)
category: Templates
order: 2
---

**Image to Image (Basic)** is one of the simplest workflows to generate images using diffusion models.

You can create stunning images with just three nodes.


<div align=center><img src="https://doc.combix.ai/doc_images/i2i.jpeg" alt="workflow" width="90%" /></div>



<br>

----

## Workflow Introduction

There are only three nodes in this basic workflow:
* Load image
* **Image to Image**
* Preview Image

<br>

```Image to image```

The ```Image to Image``` node generates images based on image prompts. 

This means you can use both image and text prompts to control the effect of the generated image. The larger the denoise parameter, the weaker the correlation between the generated image and the prompt image.

_In Combix, if you ever forget what this node does while you're working on your project, simply click on it, and the definition will appear on the right side of the page._

<br>

----

## How to use 

Welcome to our ```Image-to-Image``` feature.

Simply upload your image, choose your preferred style, and input your desired prompts. 

Once satisfied, apply ```Denoise``` for final refinement.


### Denoise
Compared to generating ```text to Image```, you will find that we now have a new parameter: ```Denoise```. 

```Denoise``` is a powerful feature that enhances the clarity of images. By reducing noise and artifacts in the image, ```Denoise``` makes the image clearer and brings out more details. 

You can control the level of image similarity by adjusting the ```Denoise```parameter to achieve different effects. 


In the following examples, we will keep the other parameters unchanged and only modify the value of ```Denoise```.

| Denoise | Results | Intensity |
| :---------:| :---------: | :---------: | 
| 0 | <img src="https://doc.combix.ai/doc_images/i2i.0.jpg" alt="workflow" width="60%" /> | Same |
| 0.5 | <img src="https://doc.combix.ai/doc_images/i2i.0.5.jpeg" alt="workflow" width="60%" /> | Slight |
| 0.75 | <img src="https://doc.combix.ai/doc_images/i2i.0.75.jpg" alt="workflow" width="60%" /> | Significant |
| 1 | <img src="https://doc.combix.ai/doc_images/i2i.1.jpg" alt="workflow" width="60%" /> | Transformative |



<br>

----


In short, we adjust the degree of change by altering the denoising strength value. The higher the denoising strength value, the greater the image transformation.



