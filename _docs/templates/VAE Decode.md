---
title: VAE Decode 
category: Nodes
order: 4
---

The **VAE Decode** node decode the latent images.

<br>

## Introduction

This node serves as a pivotal component in the process of translating latent space images back into the realm of pixel space. Based on the provided VAE, it is capable of reconstructing images, making them ready for display or subsequent download.

<br>

## Inputs

|     Name     | Explanation                  |
| :---------:| :-------------:|
| ```samples``` | The latent images to be decoded. |
| ```VAE``` | The VAE to use for decoding the latent images. |

<br>

## Outputs

|     Name     | Explanation                  |
| :---------:| :-------------: |
| ```image``` | The image reconstructed from the provided latent representation using the specified VAE model. |

<br>

## How to Use
The **VAE Decode** node is often integrated with other nodes to facilitate a seamless preview of the generated images. Here's how they typically work in tandem:

Load Checkpoint: This node supplies the ```VAE``` model necessary for the **VAE Decode** node.

* **KSampler**: This node generates the ```samples``` that the **VAE Decode** node will decode.

* **Preview Image**: This node receives the decoded ```image``` from the **VAE Decode** node and enables the preview of images directly within the node graph.

<img src="https://magmai-ai.github.io/magmai-doc/doc_images/PreviewingtheOutcome.jpg" alt="Previewing the Outcome" width="=70%" />


In the typical workflow, the latent image processed by the **KSampler** node is decoded by the **VAE Decode** node, with the results then presented in the **Preview Image** node's interface.

