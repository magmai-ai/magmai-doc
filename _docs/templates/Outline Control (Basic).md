---
title: Outline Control (Basic)
category: Templates
order: 8
---

**Outline Control (Basic)** enables for the generation and preview of images that closely resemble the reference image but are rendered in a different style.

We are introducing only one new node at this time as well.


<div align=center><img src="https://doc.combix.ai/doc_images/ocb.jpeg" alt="workflow" width="90%" /></div>




<br>

----

## Workflow Introduction

The new magic nodes have been added to this basic workflow.


* Load Image
* **Outline control**
* Text to Image
* Preview Image

<br>

```Outline Control```

The ```Outline Control``` node obtains the contour information from a picture. 

This means it detects the edges and shapes in the picture, which can be used to control the outlines of the generated picture during the creation process.

*In Combix, if you ever forget what this node does while you're working on your project, simply click on it, and the definition will appear on the right side of the page.*

<br>

----


## How to Use

Welcome to our ```Outline Control``` feature. Follow these steps to transform your image:

1. **Load Image**
   - Upload an image using the ```Load Image``` node.
   - This image will serve as the base for creating an outline and applying transformations.

2. **Outline Control**
   - Connect this node to the loaded image.
   - This node generates an outline of the input image to guide the style transfer.

3. **Text to Image**
   - Link the control to the previous ```Outline Control``` node.
   - Choose the desired style and specify a positive prompt.

4. **Preview Image**
   - Connect this node to the ```Text to Image``` node to visualize the final output.

---

## Inspirations

Explore these examples for inspiration on different styles to try out.

| Load Image | Style | Prompt | Preview Image |
| :---------:| :-------------: | :---------: | :----------:|
| <img src="https://doc.combix.ai/doc_images/ocb2.1.jpeg" alt="workflow" width="60%" /> | anime_meina_pstel | a girl | <img src="https://doc.combix.ai/doc_images/ocb2.2.jpg" alt="workflow" width="60%" /> |
| <img src="https://doc.combix.ai/doc_images/ocb1.1.jpeg" alt="workflow" width="60%" /> | anime_meina_pstel | watermelon slices | <img src="https://doc.combix.ai/doc_images/ocb1.2.jpeg" alt="workflow" width="60%" /> |



