---
title: Upscale (Basic)
category: Templates
order: 4
---

**Upscale (Basic)** is designed to enhance the overall quality of an image, making it more realistic and detailed. 

With just three simple nodes, you can effortlessly elevate your images to a new level of stunning high quality.

| Origin | Upscale |
| :--------------:| :---------: | 
| <img src="https://doc.combix.ai/doc_images/upb 1.jfif" alt="workflow" width="=300" /> | <img src="https://doc.combix.ai/doc_images/upb 1.1.jpeg" alt="workflow" width="300" /> 
| <img src="https://doc.combix.ai/doc_images/upb 2.jpeg" alt="workflow" width="300" /> | <img src="https://doc.combix.ai/doc_images/upb 2.2.jpeg" alt="workflow" width="300" /> |


<br>

----

## Workflow Introduction

There are only three nodes in this basic workflow:
* Load image
* **Image Scale**
* Image preview

<br>


<div align=center><img src="https://doc.combix.ai/doc_images/upbbb.jpeg" alt="workflow" width="90%" /></div>

<br> 

```Image Scale```

The ```Image Scale``` node scales the resolution of the image according to a certain magnification. 

This means it adjusts the size of the image by enlarging or reducing its resolution based on a specified scal

_In Combix, if you ever forget what this node does while you're working on your project, simply click on it, and the definition will appear on the right side of the page._


<br>

----
## How to Use
Welcome to our Upscale feature.

1. **```Load Image```**

- Upload your original image using the ```Load Image``` node.
- This image will serve as the base for the upscaling process.

2. **```Image Scale```**
- Connect the ```Image Scale``` node to the loaded image.
- Adjust the two parameters provided to control the scaling process.

3. **```Preview Image```**
- Connect this node to the ```Image Scale``` node to visualize the enhanced clarity of the upscaled image.

<br>


### Method

The ```Image Scale``` node offers a variety of interpolation methods, each with its own strengths and weaknesses, catering to factors such as image quality, processing speed, and desired output, thus providing flexibility in selecting the most suitable method for different scenarios.

We used the blurry image below as the original to illustrate the effect of the different methods.

<div align=center><img src="https://doc.combix.ai/doc_images/upb333 .jpg" alt="workflow" width="30%" /></div>

<br>


| Method | Explaination |  Result |
| :---------:| :----------- | :---------: | 
| ```area``` | Area method  calculates the value of a pixel by averaging the values of the pixels in its surrounding neighborhood, resulting in a smooth and continuous image.| <img src="https://doc.combix.ai/doc_images/upb-area.jpeg" alt="workflow" width="900" /> |
| ```bicubic``` |Bicubic method takes into account sixteen pixels arranged in a 4x4 grid during interpolation. <br><br> The results of *bicubic* in smoother transitions and better preservation of fine details compared to bilinear interpolation. |<img src="https://doc.combix.ai/doc_images/upb-bicubic.jpeg" alt="workflow" width="900" /> |
| ```bilinear``` |Bilinear interpolation looks at the four nearest pixels (forming a square) and takes a weighted average to figure out the color of the new pixel. <br><br> This method will smooth out the transitions between pixels, making the image look less blocky compared to nearest neighbor. |<img src="https://doc.combix.ai/doc_images/upb-bilinear.jpeg" alt="workflow" width="500" /> |
| ```lanczos``` | Lanczos considers a larger area of pixels, often in a circular or elliptical shape, and uses a mathematical function called the Lanczos kernel to calculate the new pixel's value. <br><br> This method helps preserve sharp edges and fine details better than bilinear interpolation. |<img src="https://doc.combix.ai/doc_images/upb-lanczos.jpeg" alt="workflow" width="500" /> |
| ```nearest-exact``` |This method selects the value of the pixel closest to the target from the original image. <br><br> This method is **fast**, but does not work well at larger upscale magnifications. |<img src="https://doc.combix.ai/doc_images/upb-nearest exact.jpeg" alt="workflow" width="500" /> |
| ```ultrasharp``` |Ultrasharp method uses deep learning model to infer what the missing details might be. <br><br> This method can produce remarkably sharp and detailed results, but it requires more computational power and may not always be perfect. |<img src="https://doc.combix.ai/doc_images/upb-ultrasharp.jpeg" alt="workflow" width="500" /> |





