# [README.md](http://README.md)



# Goal

Launch the Gemma3 model on GKE (Google cloud) GPU, verify, test interactively and teardown.

- store the model in cold blob storage (~ Glacier) for rapid re-deploy
- autmate entire process, with opton to leave up for interactive chat
- minimal chat endpoint and test page

# System Overview

![System Overview](./system-overview.svg)

# Rough Cost/Throughput 

## **Gemma 3 (27B dense)**

Google

### **Deployment**
- Fits on **1–2 GPUs**

| **Hardware** | **GPUs** | **tok/s**    | **$/day**    |
| ------------ | -------- | ------------ | ------------ |
| H200         | 2        | ~1,500–2,500 | **$145–240** |
| B200         | 1–2      | ~3,000–5,000 | **$150–480** |

👉 **Best small-model economics**

## **8) Mistral Small (7B)**

Mistral AI

### **Deployment**
- Single GPU

| **Hardware** | **GPUs** | **tok/s**    | **$/day**    |
| ------------ | -------- | ------------ | ------------ |
| H200         | 1        | ~2,000–4,000 | **$70–120**  |
| B200         | 1        | ~5,000–8,000 | **$150–240** |

👉 **Ultra-cheap high throughput tier**

References:
 - ChatGPT - Open Source LLM's 2026

