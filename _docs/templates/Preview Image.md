---
title: Preview Image
category: Nodes
order: 8
---

The **Preview Image** node can be used to preview images inside the node graph.

<br>

## Introduction

This node is designed for creating temporary preview images. It can generate a unique temporary file for each image, compressing the image into a zip file when there are multiple images. This is particularly useful for generating previews of images during processing.

<br>

## Inputs

|     Name     | Explanation                  |
| :---------:| :-------------:|
| ```image``` | The pixel image to preview. |

<br>

## Outputs

This node does not produce any traditional outputs; instead, it offers a visual display of the image within the node graph.

<br>

## How to Use

### Preview the Work

<img src="https://magmai-ai.github.io/magmai-doc/doc_images/PreviewtheWork.jpg" alt="Preview the Work" width="=70%" />

The **Preview Image** node can be strategically placed at various points within your workflow to offer immediate visual feedback. For instance, you might connect it to the output of a **VAE Encode** node at the end of your workflow to get a glimpse of the encoded ```image```.

Furthermore, it can be used to preview semi-finished images at intermediate stages. By connecting the **Preview Image** node to any node that outputs an ```image```, such as the **AIO Aux Preprocessor** node depicted in the figure, you can gain insights and make adjustments as needed.

This visual feedback is invaluable for **debugging** and fine-tuning your workflow.

### Download Files

To save your work for further use, simply hover your mouse over the previewed image and wait for the green download arrow to appear. Click on this arrow, and the file will be conveniently downloaded to your designated documents folder.
