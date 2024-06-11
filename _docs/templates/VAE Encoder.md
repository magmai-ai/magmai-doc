---
title: VAE Encode
category: Nodes
order: 5
---

The **VAE Encode** node encode the pixel images.

<br>

## Introduction

The **VAE Encode** node can be used to encode pixel space images into latent space images. This process involves capturing the core characteristics of the images using VAE, resulting in a compressed form that retains the essence of the original.

<br>

## Inputs

|     Name     | Explanation                  |
| :---------:| :-------------:|
| ```pixels``` | The pixel space images to be encoded. |
| ```VAE``` | The VAE to use for encoding the pixel images. |

<br>

## Outputs

|     Name     | Explanation                  |
| :---------:| :-------------: |
| ```latent``` | The latent space representation of the input image. |

<br>

## How to Use

### Image to Image workflow

The **Image to Image** workflow is a commonly used workflow processoing loaded images. You can use this workflow as an example to understand the basic use of the **VAE Encode** node.

Typically, the **VAE Encode** node is used with the following nodes:

* **Load Checkpoint**: This node supplies the ```VAE``` model necessary for the **VAE Encode** node.

* **Load Image**: This node provides the ```pixel``` image that the **VAE Encode** node will encode.

* **KSampler**: This node generates a new version of the latent image, starting from the ```latent``` provided by **VAE Encode**.

<img src="https://magmai-ai.github.io/magmai-doc/doc_images/image_to_image_0.jpg" alt="Direct Output Model" width="=70%" />

The example workflow shown above is a **Image to Image** workflow.

The **VAE Encode** node requires a pixel image as input, which can be supplied using the **Load Image** node as shown in the Image to Image workflow. This setup allows **KSampler** to generate an image from the latent representation of the pixel image, with the content influenced by any accompanying text prompts.
