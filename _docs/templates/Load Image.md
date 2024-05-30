---
title: Load Image
category: Nodes
order: 7
---

The **Load Image** node can be used to to load an image, processing it to adapt the workflow.

<br>

## Introduction

This node can load an image, which can be uploaded by starting the file dialog or by dropping an image onto the node.

It handles image formats with multiple frames, applies necessary transformations such as rotation, normalizes pixel values. This node is essential for preparing images for further processing or analysis within a workflow.

<br>

## Inputs

|     Name     | Explanation                  |
| :---------:| :-------------:|
| ```image``` | The image file that is uploaded. |

<br>

## Outputs

|     Name     | Explanation                  |
| :---------:| :-------------: |
| ```image``` | The processed image with pixel values normalized, ready for further analysis. |
| ```mask``` | The alpha channel of the image. |

### ```mask```

The ```mask``` output is particularly useful when dealing with images that contain transparency, such as PNGs. 

It generates a ```mask``` where transparent areas are marked as 0 (white) and opaque areas as 1 (black). If the image lacks a transparent channel, a ```mask``` with all values set to 1 is generated, indicating full opacity. It's important to note that only the transparent parts of the image will be affected by workflow.

|     Mask Shape     | result                  |
| :---------:| :-------------: |
|  |  |
|  |  |

In the table, the distinction between transparent and non-transparent areas in ```mask``` significantly influences the content of the resulting images. To encourage the use of ```mask```, a more convenient method is provided, which will be detailed below.

<br>

## How to Use

### Use as a pixel Input

The **Load Image** node can be employed to load ```images``` for a multitude of nodes. In any given workflow, simply connect the **Load Image** node to any node that requires an image input, such as the **AIO Aux Preprocessor** node shown in the figure.

<img src="https://magmai-ai.github.io/magmai-doc/doc_images/DirectOutputModel_0.jpg" alt="Direct Output Model" width="=70%" />

### Image Inpainting

The **Image Inpainting** workflow is an adaptation of the **Image to Image** workflow, providing a clear example of how the **Load Image** node can serve as a ```mask``` provider.

In the **Image Inpainting** workflow, the **Load Image** node is typically paired with the following nodes:

* **Convert Image to Mask**: This node transforms the input ```image``` into a usable ```mask```.

* **VAE Encode (for inpainting)**: An advanced version of the **VAE Encode node**, which encodes both the ```image``` and the ```mask``` into the latent space.

<img src="https://magmai-ai.github.io/magmai-doc/doc_images/DirectOutputModel_0.jpg" alt="Direct Output Model" width="=70%" />

In this workflow, the **Load Image** node is used to load a black and white ```image```. Instead of utilizing the ```mask``` output directly from the **Load Image** node, the **Convert Image to Mask** node is employed to convert it into a ```mask``` that allows modifications only in white areas. 

Utilizing this ```mask```, **VAE Encode (for inpainting)** encodes both the ```image``` and the ```mask``` into the latent space. This process ensures that the **KSampler** modifies the image only within the designated areas, based on the provided text prompt.


