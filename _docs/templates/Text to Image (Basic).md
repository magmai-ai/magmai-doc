---
title: Text to Image (Basic)
category: Templates
order: 1
---

**Text to Image (Basic)** is one of the simplest workflows to generate images using diffusion models.

You can generate stunning images by only 2 nodes. 

<div align=center><img src="https://doc.combix.ai/doc_images/t2i.jpeg" alt="workflow" width="90%" /></div>

<br>

<iframe width="560" height="315" src="https://www.youtube.com/embed/Dm-ygByuv-M" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br>

----

## Workflow Introduction

There are only two nodes in this basic workflow:
* Text to Image.
* Preview Image.

<br>

```Text to Image```


The ```Text to Image``` node generates pictures directly from text descriptions. 

This means you can type in a description of what you want to see, and the node will create an image based on that text.

<br>

----

## How to Use

In this template workflow, you can control the content and the style of the generated image.


### Style
You can choose different styles in the ```Text to Image``` node.

 In Combix, We offer a **wide** array of styles to choose from. 

In the example below, we keep prompt consistent but change different style to show the effect.

| Param      | Value |  Results |
| :-----------: | :-----------: | :-----------: |
| style      | anime_blue_pencil       |  <img src="https://doc.combix.ai/doc_images/txt2img_anime0.jpg" alt="workflow" width="60%" /> |       
| style       | realistic_realvis                    |  <img src="https://doc.combix.ai/doc_images/txt2img_real0.jpg" alt="workflow" width="60%" /> |

<br>

We have also added some special and interesting styles. Starting from ‘realistic_realvis,’ these styles use base models with strong stylistic tendencies. This means that other parameters do not significantly influence the styles’ inherent characteristics

Preview Function: To enhancing your browsing experience, **just hover your cursor over the style names, and a preview will appear on the left side.** 

<img src="https://doc.combix.ai/doc_images/fcb.2.jpeg" alt="workflow" width="60%" />



### pos_prompt

The ```pos_prompt``` param of the ```Text to Image``` node controls the content of the generated image. 

Describe the content of your picture, and it will be generated accordingly as soon as possible.

| Param      | Value |  Results |
| :-----------: | :-----------: | :-----------:|
| pos_prompt      | 1girl, smile, half body       |  <img src="https://doc.combix.ai/doc_images/txt2img_real0.jpg" alt="workflow" width="60%" />|       
| pos_prompt       | sleeping cat                    |  <img src="https://doc.combix.ai/doc_images/txt2img_real2.jpg" alt="workflow" width="60%" />  |


<br>

----

## Others
Click the node, and there will be an introduction to this node and an editing panel for advanced parameters in the right panel. 

By changing these parameters, you can alter the effect of the output.


| Param      | Explaination | 
| :-----------: | :-----------: |
| width, height      | The size of the generated image.       |   
| neg_prompt       | A description of the content you don't want to <br> appear in the generated image.    |   
| control       | You can link one or more image generation control nodes <br> to the ```Text to Image``` node <br>to further control the result of image generation.  |  


<div align=center><img src="https://doc.combix.ai/doc_images/t2i panel.jpeg" alt="workflow" width="40%" /></div>


