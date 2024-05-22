---
title: Style Reference (Basic)
category: Templates
order: 7
---

**Style Reference (Basic)** allows for the generation and preview of images that combines the base photo with the chosen style, prominently featuring the specified element in a realistic yet artistically enhanced manner.


We are introducing only one new node at this time as well.


<div align=center><img src="https://doc.combix.ai/doc_images/srb.jpeg" alt="workflow" width="90%" /></div>




<br>

----

## Workflow Introduction

The new magic nodes have been added to this basic workflow.


* Load Image
* **Image style control**
* Text to Image
* Preview Image

<br>

```Image Style Reference```

The ```Image Style Reference``` node obtains the style information from a picture.

This means it analyzes elements like colors, textures, and overall aesthetic, which are then used to control the style effect of the generated picture.

*In Combix, if you ever forget what this node does while you're working on your project, simply click on it, and the definition will appear on the right side of the page.*

<br>

----


## How to Use

Welcome to our ```Style Reference``` feature.


1. ```Load Image```
   - Upload an image.
   - This image will be the base for applying the style and transformations.

2. ```Image Style Reference```
   - Weight: Enhances the style's influence on the image.
   - Start_at: The style starts applying after 30% of the transformation process.
   - Connect this to the loaded image.

3. ```Text to Image```
   -  Link the control to the previous ```Image style reference``` node.
   -  Choose the desired style and specify a positive prompt.
   

4. ```Preview Image```
   - Connect to the ```Text to Image``` node to visualize the final output.

<br>


By following these steps, you can create visually stunning images with ease. 

Feel free to experiment with different styles and prompts to see how they affect the final result. 

<br>

## Inspirations


Explore these examples for inspiration on different styles to try out.

| Reference | Style| Prompt | Preview Image |
| :---------:| :------: | :-------------: | :---------: | 
| <img src="https://doc.combix.ai/doc_images/srb 1.1.jpg" alt="workflow" width="60%" /> | realistic_realvis | a cat: 1.3 | <img src="https://doc.combix.ai/doc_images/srb 1.2.jpg" alt="workflow" width="60%" /> |
| <img src="https://doc.combix.ai/doc_images/srb.2.1.jpeg" alt="workflow" width="60%" /> | realistic_realvis | a capybara and a dog: 1.3 | <img src="https://doc.combix.ai/doc_images/srb 2.2.jpg" alt="workflow" width="60%" /> | 




