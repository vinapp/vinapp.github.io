---
layout: post
title: Multi class image generation using Stable Diffusion
date: 2022-09-31 06:00:00-0400
description: Voice based Multi class image generation using Stable Diffusion
tags: ai ml
giscus_comments: false
related_posts: false
toc:
  beginning: true
---

## Voice based Multi class image generation using Stable Diffusion

### Problem Statement:

We have seen the generative models like Diffusion Model for some time. With the release of Stable Diffusion's (released recently as early as August 2022) the code and the model weights have been released publicly allowing users to have more control over the topic picture and then controlling the diffusion model using text-based inputs, we can do a transfer learning for a subject & an identifier with just few images. Also, we see that there are only few articles on these and especially only covering a single class transfer learning. So, taking advantage of this we see an option of training (our own set of images) with different classes (with our own identifiers) and clubbing multiple classes. So with this we can issue a single sentence/text which covers all the classes/identifiers and generate images based our custom image set. Also, extending text-to-image to voice-to-text-to-image helps.

### Task:

  - For our own set of images train with the pre-trained model with multiple classes/subjects and the identifier's
  - Add a support to speech to text option on top of text to image option
  - Find the group of classes/subject that we want to train and test the same with different text's (sentences). Testing could be manual or based on the labelled data.

### Why is it interesting ?

Interesting because imagination becomes real in the image. One of the powerful use case would be in slide preparation or storyboard creation wherein we can generate images on our own set of images (grouped into different class) that are trained via transfer learning. This would save time and also have multiple imaginative image generation options. Also, here we have some control over the image generation since its operating on our own set of images.

Also, although there are articles/blogs on stable diffusion (past 2 months) on training individual class (CAT/DOG et) but we haven't seen any articles (so far) on how we can use set/group of images and how we can iteratively create multiple classes one of top of each other along with publicly available dream booth diffusion model data. So, this could be a nice candidate for publishing a blog that would be very useful to people.

Eg:

**photo of \<custom-identifier\> \<class-name\>**

- photo of \<xyz\> \<temple\> ---\> Single class
- photo of \<kar\> \<forest\> ---\> Single class
- photo of \<xyz\> \<temple\> in \<kar\> \<forest\> and sunlight ---\> Mixing multiple custom classes

This one especially touches all/most of ML aspects like deep learning, un-supervised, synthesized data, labelled data, text summarization, voice to text, text to image etc. This one will serve as a nice learning experience for all of us.

Example Usecase: Think of having a plugin (to powerpoint/google slides) that can integrate custom generative model to generate our own choice of images and this would be very powerful... For eg: Every week if we need to publish some articles (say related to temples) and I need some creative images and it's very difficult to get the images of our own choice and that too for say 100's of articles. So in that case this is very useful and we don't have bother out [licensing](https://huggingface.co/CompVis/stable-diffusion) issues as well unless it's not misused.

### Data

  - To start with we require only few sets of images for transfer learning
  - Verifying the result is a bit challenging but we could leverage the labelled data.

### Methods to experiment

  - For transfer learning we use different sets of custom images for different classes. The new class we train will be on top of the previous classes. At the end we give the instruction in the form of speech or text (that covers all the classes and identifiers) to generate the synthesized images.

Example images generated from stable diffusion model:
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/multi-class-image-generation-stable-diffusion.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

### Evaluate your results

**Aspects**

  - Fidelity: the quality of the generated samples. Measures how realistic the images are. You can think of it as how different each fake sample is from its nearest real sample.
  - Diversity: the variety of the generated samples. Measures how well the generated images cover the whole diversity or variety of the real distribution.

Planning to use the labelled trained images to match against the generated images and for this we need more images to train the labelled data.

** Quantitative Results:**

**NA/?**

** Quantitatively Analysis:**

**NA/?**

** What is the hypothesis regarding the results compared to baselines**

  - It can be created into a product (powerpoint, word, google slides, browser plugins etc) for practical use.
  - Choosing the classes, identifiers sequences will surely help in synthesized images of our own set of images.

** References:**

- [Stable Diffusion](https://en.wikipedia.org/wiki/Stable\_Diffusion)
- [Dream booth Diffusion](https://arxiv.org/pdf/2208.12242.pdf)
- [Diffusion Model]([https://en.wikipedia.org/wiki/Diffusion\_model](https://en.wikipedia.org/wiki/Diffusion_model))
- [Stable Diffusion Model](https://huggingface.co/CompVis/stable-diffusion)

** Related Works Article:**

- [Train Stable Diffusion Model](https://techpp.com/2022/10/10/how-to-train-stable-diffusion-ai-dreambooth/)
- [Fine Tune Stable Diffusion Model](https://bytexd.com/how-to-use-dreambooth-to-fine-tune-stable-diffusion-colab/)
