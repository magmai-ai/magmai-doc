---
title: Pose Control (Basic)
category: Templates
order: 3
---

**Pose Control (Basic)** allows for the wasy generaetion of images with a wide variety of human poses. 

Introducing only one new node this time as well.

<div align=center><img src="https://doc.combix.ai/doc_images/pcbbb.jpeg" alt="workflow" width="90%" /></div>



<br>

----

## Workflow Introduction

The new magic nodes have been added to this basic workflow.

* Load Image
* **Pose control**
* Text to Image
* Preview Image

<br>

```Pose control```

The ```Posture Control``` node obtains the posture information of the characters in the picture. 

This means it analyzes and extracts the poses and positions of the characters, which can be used to control their posture when the picture is generated.

_In Combix, if you ever forget what this node does while you're working on your project, simply click on it, and the definition will appear on the right side of the page._

<br>

----


## How to Use

Welcome to our `Pose Control` feature!

1. **Upload Image:** Start by uploading your picture into the `Posture Control` node.

2. **Preview Image:** Connect it to the `Preview Image` node to see the initial setup.

3. **Set Up Control:** Then, in the `Posture Control` node, find `image_gen_control` and connect it to the `Text to Image` node. Be sure to add your desired `pos_prompt`.

4. **Generate Image:** Finally, generate your new image and review the results.




<br>

## Inspirations

Check out these inspirations for some cool poses to try.

| Load Image | Preview Posture | Preview Image |
| :---------:| :-------------: | :---------: | 
| <img src="https://doc.combix.ai/doc_images/pcb 1.jpeg" alt="workflow" width="60%" /> | <img src="https://doc.combix.ai/doc_images/pcb 1.1.jpeg" alt="workflow" width="60%" /> | <img src="https://doc.combix.ai/doc_images/pcb 1.1.1.jpeg" alt="workflow" width="60%" /> |
| <img src="https://doc.combix.ai/doc_images/pcb 2.jpeg" alt="workflow" width="60%" /> | <img src="https://doc.combix.ai/doc_images/pcb 2.2.jpg" alt="workflow" width="60%" /> | <img src="https://doc.combix.ai/doc_images/pcb 2.2.2.jpeg" alt="workflow" width="60%" /> |

