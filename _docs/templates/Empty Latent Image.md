---
title: Empty Latent Image 
category: Nodes
order: 3
---

The **Empty Latent Image** node can be used to create a new set of empty latent images. They can then be used inside workflows by noising and denoising.

<br>

## Introduction

This node can generate a blank latent space representation with specified dimensions and batch size as you require. It serves as a foundational step in generating or manipulating images in latent space, providing a starting point for further image processes.

<br>

## Inputs

|     Name     | Explanation                  |
| :---------:| :-------------:|
| ```width``` | The width of the latent images in pixels (between range 16 - 16384). |
| ```height``` | The height of the latent images in pixels (between range 16 - 16384). |
| ```batch_size``` | The number of latent images. |

<br>

## Outputs

|     Name     | Explanation                  |
| :---------:| :-------------: |
| ```latent``` | The empty latent images. |

<br>

## How to Use
### A Single Image

The **Empty Latent Image** node is typically used in conjunction with this node:

* **KSampler**: This node generate a new version of the empty ```latent image``` provided by **Empty Latent Image**.

<img src="https://magmai-ai.github.io/magmai-doc/doc_images/ASingleImage.jpg" alt="A Single Image" width="=70%" />

In this workflow, **Empty Latent Image’s** batch_size is one, creating a single empty ```latent image``` for **KSampler**. By doing this, you will generate an image from a blank initial image, and the generated image content will be largely determined by your text prompt.

### A Series of Images

Not every generated image will meet our expectations, especially when text prompts are too simple or complicate. This may leads to a time-consuming and labor-intensive process. At this point, we can improve work efficiency by increasing the ```batch_size``` of the **Empty Latent Image**.

<img src="https://magmai-ai.github.io/magmai-doc/doc_images/ASeriesofImages.jpg" alt="A Series of Images" width="=70%" />

In this workflow, the ```batch_size``` of the **Empty Latent Image** is set to 16, resulting in 16 final images being generated. While they are not identical, they do share similar content and style as per your requirements. You can choose the one you are most satisfied with from these images. 

By obtaining more image options at once, you have the flexibility to choose the value of ```batch_size```. However, be cautious as excessively large values can also lead to an increase in running time.
