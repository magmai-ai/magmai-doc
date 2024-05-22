---
title: Face Control (Basic)
category: Templates
order: 5
---

**Face Control (Basic)** facilitates effortless facial adjustments with thousands of styles to choose from.

We are introducing only one new node at this time as well.

<div align=center><img src="https://doc.combix.ai/doc_images/fcb.jpeg" alt="workflow" width="90%" /></div>




<br>

----

## Workflow Introduction

The new magic nodes have been added to this basic workflow.
* Load Image
* **Face control**
* Text to Image
* Preview Image

<br>

```Face control```

The ```Face Control``` node obtains face ID information.

 This means it identifies and extracts facial features, which can be used to generate the face of a specific person in image generation. 

_In Combix, if you ever forget what this node does while you're working on your project, simply click on it, and the definition will appear on the right side of the page._


<br>

----

## How to Use

Welcome to our ```Face Control``` feature. Follow these steps to transform your image:

1. **Load Image**
   - Upload an image using the ```Load Image``` node.
   - This image will serve as the base for creating an outline and applying transformations.

2. **Face Control**
   - Connect this node to the loaded image.
   - This node identifies and extracts facial features of the input image to guide the style transfer.

3. **Text to Image**
   - Link the control to the previous ```Outline Control``` node.
   - Choose the desired style and specify a positive prompt.

4. **Preview Image**
   - Connect this node to the ```Text to Image``` node to visualize the final output.



<br>


## Face Control


Within this node, there are five parameters. 

When presenting examples, we maintain the consistency of the other parameters while adjusting specific ones to observe the effects of their intensity.


|     Name     | Explanation                                                                 | Intensity | Result                                                                          |
|:------------:|:---------------------------------------------------------------------------:|:---------:|:-------------------------------------------------------------------------------:|
|    ```weight```    | Controls the influence of the face control on the final image generation.   | 0.7       | A balanced application of the face control, ensuring the generated image closely follows the facial features of the original image. |
| ```lora_weight```  | Adjusts the weight of the low-rank adaptation (LoRA) in the image generation process. | 0.7       | Enhances the specific style or adaptation effect applied to the face in the generated image. |
|   ```start_at```   | Defines the starting point in the image generation process where face control begins to take effect. | 0         | Face control influences the image generation from the very beginning.            |
|    ```end_at```    | Specifies the end point in the image generation process where face control stops being applied. | 1         | Face control is applied throughout the entire image generation process.           |
|   ```control```    | A boolean parameter that toggles the activation of the face control feature. | On        | When enabled, face control is active and influences the image generation based on the set parameters. |

**Examples:**

```start_at``` = 0, ```end_at``` = 1: Face control is applied throughout the entire generation process. This setting ensures that the facial features are consistently controlled from the start to the end, resulting in a coherent and accurate depiction of the face in the final image.

<div align=center><img src="https://doc.combix.ai/doc_images/fcb.jpeg" alt="workflow" width="90%" /></div>

<br>

```start_at``` = 0.2, ```end_at``` = 0.8: Face control is applied starting from 20% into the generation process and stops at 80%. This might be used if you want the initial and final touches of the image to be less influenced by face control, perhaps to blend more naturally with other stylistic elements.

<div align=center><img src="https://doc.combix.ai/doc_images/fcb.1.jpeg" alt="workflow" width="90%" /></div>


<br>

## Inspirations 

Please note that in Combix, we offer a **wide** array of styles to choose from.

We have also added some special and interesting styles. Starting from 'realistic_realvis,' these stlyes use base models with strong stylistic tendencies. This means that other parameters do not significantly influence the styles' inherent characteristics

Preview Function: To enhancing your browsing experience, **just hover your cursor over the style names, and a preview will appear on the left side.**

<div align=center><img src="https://doc.combix.ai/doc_images/fcb.2.jpeg" alt="workflow" width="90%" /></div>

<br>


Explore these examples for inspiration on different styles to try out.

| Load Image | Style | Prompt | Preview Image |
| :---------:| :-------------: | :---------: | :----------:|
| <img src="https://doc.combix.ai/doc_images/fcb 1.jpeg" alt="workflow" width="60%" /> | anime_blue_pencil | 1 girl, smile, <br> half body | <img src="https://doc.combix.ai/doc_images/fcb blue pencil.jpeg" alt="workflow" width="60%" /> |
| <img src="https://doc.combix.ai/doc_images/fcb 1.jpeg" alt="workflow" width="60%" /> | misc_gothic | 1 girl, emotionaless face, <br> half body | <img src="https://doc.combix.ai/doc_images/fcb_gothic.jpeg" alt="workflow" width="60%" /> |
| <img src="https://doc.combix.ai/doc_images/fcb 1.jpeg" alt="workflow" width="60%" /> | artstyle_art_nouveau | 1 girl, angry, <br>half body | <img src="https://doc.combix.ai/doc_images/fcb_nouveau.jpeg" alt="workflow" width="60%" /> |


