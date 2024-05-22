---
title: Face + Pose Control (Basic)
category: Templates
order: 6
---

**Face + Pose Control (Basic)** allows for the generation and preview of images with customized facial features and postures.

While there may appear to be many nodes, they have already been introduced. This tutorial integrates face and pose control methods to provide comprehensive control over image customization.


<div align=center><img src="https://doc.combix.ai/doc_images/fpcb .jpg" alt="workflow" width="90%" /></div>




<br>

----

## Workflow Introduction

Remove the duplicate nodes, there are actually only five nodes in this basic workflow.


* Load Image
* Face Control
* Posture Control
* Text to Image
* Preview Image

<br>

----


## How to Use

Welcome to our ```Face + Pose Control``` feature.

1. **Start by dragging out two `Load Image` nodes**: Select two photos that you want to combine.

2. **Navigate to the `Face Control` and `Posture Control` nodes**:
    - Connect the photo with the desired facial features to the `Face Control` node.
    - Connect the photo with the pose to the `Posture Control` node.

3. **Link the nodes**:
    - Connect the ```Face Control``` node to the `Posture Control` node.
    - Then, connect the `image_gen_control` output from the `Posture Control` node (which is already linked to `Face Control`) to the `control` input in the `Text to Image` node.

4. **Choose your style and write a prompt**:
    - In the `Text to Image` node, pick the style you like.
    - Write a creative prompt to describe the image you want to generate.

5. **Preview your new image**:
    - Check out the final image created based on your inputs.

---



<br>

## Inspirations


Explore these examples for inspiration on different styles to try out.

| Face Image | Posture Image | Preview Image |
| :---------:| :-------------: | :---------: | 
| <img src="https://doc.combix.ai/doc_images/fpcb.1.1.jpeg" alt="workflow" width="60%" /> | <img src="https://doc.combix.ai/doc_images/fpcb.1.2.jpeg" alt="workflow" width="60%" /> | <img src="https://doc.combix.ai/doc_images/fpcb.1.3.jpg" alt="workflow" width="60%" /> |
| <img src="https://doc.combix.ai/doc_images/fpcb.2.1.jpeg" alt="workflow" width="60%" /> | <img src="https://doc.combix.ai/doc_images/fpcb.2.2.jpeg" alt="workflow" width="60%" /> | <img src="https://doc.combix.ai/doc_images/fpcb.2.3.jpg" alt="workflow" width="60%" /> |


