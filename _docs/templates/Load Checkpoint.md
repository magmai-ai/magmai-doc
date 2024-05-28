---
title: Load Checkpoint
category: Nodes
order: 1
---

**Load Checkpoint** node is a fundamental component to load a diffusion model, which are used to denoise latents. This node will also provide the appropriate VAE and CLIP model.


<br>

## Introduction

This node operates as a selector. It selects the appropriate model based on the ckpt_name chosen by user. It also provide the clip model used for encoding text prompts and the vae model used for encoding and decoding images to and from latent space. 

Think of Load Checkpoint as the power source of a circuit, generating three distinct currents: model, vae, and clip. By connecting wires to corresponding nodes, you can activate their functions.
<br>


## Inputs

|     Name     | Explanation                  |
| :---------:| :-------------|
| ```ckpt_name``` | The checkpoint use for diffusion model. |


<br>

## Outputs

|     Name     | Explanation                  |
| :---------:| :-------------: |
| ```model``` | The model used for workflow. |
| ```vae``` | The VAE model used for encoding and decoding images to and from latent space. |
| ```clip``` | The CLIP model used for encoding text prompts. |


<br>

## How to Use

### Direct Output Model

For most workflows,such as **Text to Image**, using the model provided by **Load Checkpoint** is effective enough.
Typically, it is used with the following nodes:

* **CLIP Text Encode (Prompt)**: This node can encode a text prompt using the CLIP model into an embedding conditioning for the sampling process that **KSampler** perform.
* **KSampler**: This node uses the model provided and the conditioning to generate a new version of the given latent.
* **VAE Decode**: Using the VAE, this node decodes the latent image data output by KSampler into ordinary image data before we can view it.

<img src="https://magmai-ai.github.io/magmai-doc/doc_images/DirectOutputModel_0.jpg" alt="Direct Output Model" width="=70%" />

<br>

The example workflow shown above is a simple **Text to Image** workflow.

In this workflow, **Load Checkpoint** is the sole source of model, vae, and clip outputs, with any node requiring them connected accordingly. This enables the nodes to function as intended.


### Output Model from Lora

Sometimes, the model from **Load Checkpoint** may be not good enough. In such cases, constructing smaller, more agile models based on the diffusion model is necessary, with **Load LoRA** being a popular choice.
* **Load LoRA**: This node can modify the diffusion model and CLIP model to change the way Latent data is denoised.


<img src="https://magmai-ai.github.io/magmai-doc/doc_images/OutputModelfromLora_0.jpg" alt="Output Model from Lora" width="=70%" />


