---
title: "RAG Reversal: An LLM as a Documentation Assistant with LoRa?"
collection: talks
type: "Talk"
permalink: /portfolio/meta7b
venue: null
date: 2024-06-06
location: null
---

Training an LLM with LoRa to create a documentation assistant that can intelligently respond to a user's queries. I used a web-scraped documentation of the Unreal Engine 5.1.

[Bublint](https://github.com/bublint/ue5-llama-lora/commits?author=bublint) has this project on their GitHub, and explained how without any LoRa training on the latest Unreal Engine documentation, both ChatGPT and Meta’s 7b LLM were out of context when asked about any questions specific to the document.

So he trained it with LoRa and the LLM demonstrated more awareness of the topic. Bublint suggested that this could perhaps be a replacement to vector databases. Quite frankly, I don’t know how much research in this field yields results robust enough to replace vector databases. But I’ve seen his work and other people’s work that demonstrates that training with LoRa is able to bring a huge amount of awareness to the LLM.


The idea of training an LLM on raw text and not following a dataset format excites me. I decided to follow through and attempt this on Meta’s 7b reformatted for Hugging Face. Although, unlike Bublint, my fine-tuning values varied and hence my model took 11 hours instead to train on an RTX 4090.
Technical specifications:

-Loaded in 8-bit

-My alpha value is 1.5

-LoRa Rank is 256, LoRa Alpha is 512

-Epochs: 5

-I stopped at loss 1.5 and I trained every layer, not just K and V.

My results were affirmative of the effect of training a model with LoRa.

This was the model before the LoRa training:

<img src='https://asaiyru99.github.io/asaiy/images/sc4.png' alt='Description of the image'>

This was the model after the training:

<img src='https://asaiyru99.github.io/asaiy/images/sc1.png' alt='Description of the image'>



