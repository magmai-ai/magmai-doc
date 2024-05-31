# Combix.ai Doc

This is the document repo of [Combix.ai](https://combix.ai/).

**Combix.ai** is a one-stop AI workflow tool designed to provide more users with professional and convenient ai workflow creation services.



## Page

* Combix: [https://combix.ai](https://combix.ai)
* Combix Doc: [https://doc.combix.ai](https://combix-ai.github.io/combix-doc/)


<br>

## How to add contents

### 1. How to add a new page
所有的文档内容页面，都放在 **_doc**文件夹下面，对于任意的新的文档页面，请在这个文件夹下面的合适位置新建一个 *.md*文件。

请记住，文档的内容只以 markdown文件格式编写。

新建的.md文件需要有固定的开头，格式如下：
```
---
title: Text to Image (Basic)
category: Templates
order: 1
---

```
其中：
* title是这个文档的标题，会显示在侧边栏中。
* category: 是这个文档在左侧边栏的分类。
* order：是这个文档在侧边栏显示的顺序。

.md文件中的其他内容，则会如实显示在网页上。
一个示例的文档，可以参考： templates/Text to Image (Basic).md

<br>

### 2. How to add a image to my page
想要在文档中插入一个图片。

首先需要将你的图片放到 **_doc/doc_images**文件夹下面。

> 注意，最好先将图片转成jpg格式的，因为这种格式的图片比较小，网页上比较好加载。

<br>

然后，在你的文档中，插入下面的语句：
```
<div align=center><img src="https://doc.combix.ai/doc_images/xxxxx.jpg" alt="workflow" width="90%" /></div>
```
其中，*xxxxx.jpg*需要替换成你实际图片在 *doc_images*文件夹下的文件路径。

例如，我有一个图片，路径是： *_docs/doc_images/txt2img.jpg*， 那么上面的内容就变成：
```txt
<div align=center><img src="https://doc.combix.ai/doc_images/txt2img.jpg" alt="workflow" width="90%" /></div>
```

上面的语句的其他几个值的说明：
* center 表示这个图片需要放在网页的中间位置。
* workflow 这个值表示当图片因为某种原因挂了的时候，会在网页上显示的替代文字。
* 90% 表示图片的宽占网页中间内容部分的90%.


<br>

### 3. How to add a video to my page

如果想要在文档中插入视频。

首先，请先将视频上传到我们youtube账号上。(https://www.youtube.com/@combix_ai)

然后，将下面的代码拷到你的文档中。

```
<iframe width="560" height="315" src="https://www.youtube.com/embed/bgcF5lkKGI4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

现在只要修改中间的链接就可以了。如果视频的youtube链接是：
```
https://www.youtube.com/watch?v=bgcF5lkKGI4
```
上面的链接中，最后面的*bgcF5lkKGI4*是视频的id，换成可以嵌入到我们网页的链接形式：
```
https://www.youtube.com/embed/bgcF5lkKGI4
```
也就是说
```
https://www.youtube.com/embed/ + 视频id
```
就是我们需要用的youtube视频链接。



## Document Requirements

文档编写时，在内容上需要尽可能符合一定的要求。

首先，对于介绍模板的文档，在内容上，需要包含以下的几个部分：
* 开头一段话，需要说明这个模板的功能是什么。
  * 可以包含工作流的截图
  * 以及对应的教学视频
* 介绍这个工作流本身：
  * 介绍工作流主要包含哪些部分，都是做的什么
* 介绍用户可以怎么使用这个模板。
  * 告诉用户，修改的重要参数有哪些，修改后会怎么样影响结果。
  * 尽可能展示不同参数修改后的效果
* 最后是其他说明


## Document Directory

目标的文档结构如下：


- [ ] Overview
  - [x] Combix Editor
- [ ] Models and Tools
  - [ ] Diffusion Checkpoints
  - [ ] Loras
  - [ ] Controlnets
  - [ ] Ipadapters
  - [ ] Combix Styles (暂不做)
- [ ] Templates
  - [x] Text to Image (Basic)
  - [ ] Text to Image
  - [x] Image to Image (Basic)
  - [ ] Image to Image
  - [ ] Image Inpainting
  - [x] Pose Control (Basic)
  - [ ] Pose Control
  - [x] Face Control (Basic)
  - [ ] Face Control
  - [x] Style Reference (Basic)
  - [x] Outline Control (Basic)
  - [x] Face + Pose Control (Basic)
  - [x] Upscale (Basic)
  - [ ] Upscale
  - [ ] Controlnets
  - [ ] Loras
  - [ ] LCM SD15
  - [ ] LCM SDXL
  - [ ] Text to Video (SVD)
  - [ ] Image to Video (SVD)
  - [ ] AnimateDiff
  - [ ] Video Style Transfer
- [ ] Nodes

  **Basic**
  - [ ] Primitive Nodes
  - [ ] Text to Image
  - [ ] Image to Image
  - [ ] Face Control
  - [ ] Posture Control
  - [ ] Image Style Reference
  - [ ] Outline Control
  - [ ] Common Effect Control (节点功能设计不完整，暂不做)
  - [ ] Image Segmentation
  - [ ] Image Scale
  - [ ] Image HD
  - [ ] Limit Image Resolution
  - [ ] Image Flip
  - [ ] Image Rotation
  - [ ] Get Image Size And Count
  - [ ] Convert Text To Data
  - [ ] XYGrid Execute
  - [ ] XYGrid Plot
  
  **Advanced**
  - [ ] Load CheckPoint
  - [ ] Load ControlNet Model
  - [ ] Load LoRA
  - [ ] Load VAE
  - [ ] CLIP Text Encode (Prompt)
  - [ ] Empty Latent Image
  - [x] KSampler
  - [ ] KSampler (Advanced)
  - [ ] VAE Decode
  - [ ] VAE Encode
  - [ ] VAE Encode (for Inpainting)
  - [ ] Load Image
  - [ ] Load Image (as Mask)
  - [ ] Load Image Batch
  - [ ] Save Image
  - [ ] Preview Image
  - [x] Apply ControlNet
  - [ ] Apply ControlNet (Advanced)
  - [ ] Convert Image to Mask

  **Plugin:Controlnet_aux**
  - [ ] AIO Aux Preprocessor
  - [ ] Canny Edge
  - [ ] DensePose Estimator
  - [ ] DWPose Estimator
  - [ ] OpenPose Pose
  - [ ] Depth Anything
  - [ ] Zoe Depth Anything
  - [ ] Inpaint Preprocessor
  - [ ] Anime Lieart (aka lineart_anime_denoise)
  - [ ] Standard Lineart
  - [ ] M-LSD Lines
  - [ ] Tile
  - [ ] Pixel Perfect Resolution

- [ ] How to Use
  - [ ] How to Import ComfyUI Workflow
  


## Content Requirements

### Nodes

节点文档的写法可以参考**KSampler** 和 **Apply ControlNet**这两个节点的教学文档。


对于每个节点的文档，至少需要包含以下的内容：

* 一到两句话的简介：放在文档开头，简明扼要说明这个节点的功能。这个简介后续也会放到combix编辑器的节点说明中。
* 1 Introduction：原理介绍，节点功能的深度说明和解释
* 2 Inputs: 输入参数的说明。至少需要说明每个参数是什么，如果可以，对于一些重要参数，可以给出不同值时的效果对比（参考Apply ControlNet文档）。
* 3 Outputs: 输出参数的说明
* 4 How to Use: 需要结合不同的使用场景，介绍这个节点的用法，例如和什么节点搭配一起使用，在这个场景中节点是发挥什么作用等，尽可能选取典型有代表性的例子。
* 5 其它按需增加 