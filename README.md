# 🎨 RealVis Image Studio
*A Highly Optimized, Photorealistic AI Image Generator for Google Colab*

[![Python](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
[![Gradio](https://img.shields.io/badge/UI-Gradio_4.44.1-orange.svg)](https://gradio.app/)
[![PyTorch](https://img.shields.io/badge/Framework-PyTorch-ee4c2c.svg)](https://pytorch.org/)
[![Model](https://img.shields.io/badge/Model-RealVisXL_V4.0-purple.svg)](https://huggingface.co/SG161222/RealVisXL_V4.0)

**RealVis Image Studio** is a streamlined, single-page web application built to generate breathtaking, highly accurate images using the `RealVisXL_V4.0` model. It features a Fooocus-inspired prompt expansion system and extreme VRAM optimizations, allowing massive 6.5GB+ models to run smoothly on free-tier Google Colab T4 GPUs without crashing.

---

## 🚀 Overview

While standard corporate base models often struggle with complex prompts, anatomical accuracy, or restrictive safety filters, this studio leverages community-trained weights to deliver uncompromising photorealism and strict prompt adherence. Whether you are generating clinical medical diagrams, cinematic concept art, or breathtaking portraits, this engine handles it with ease.

## ✨ Key Features

* **🧠 Advanced Brain Transplant (RealVisXL):** Uses a highly fine-tuned SDXL model for superior anatomy, lighting, and photorealism compared to standard base models.
* **🎨 Fooocus-Style Prompt Expansion:** Choose a visual style (e.g., Cinematic, Digital Art, Photographic) and the engine automatically wraps your prompt in optimized positive and negative keywords.
* **📏 Dynamic Aspect Ratios:** Select standard resolutions (Square, Portrait 3:4, Landscape 16:9, etc.) instantly from a dropdown. No math required.
* **⚙️ Advanced Generation Control:** Fine-tune the AI's creativity using dynamic **CFG Scale** (Prompt Adherence) and **Inference Steps** sliders.
* **⚡ Extreme VRAM Optimization:** Engineered specifically to bypass Colab's 15GB memory ceiling using:
  * PyTorch `expandable_segments` memory defragmentation.
  * VAE Tiling & Slicing to prevent memory spikes during final image decoding.

---

## 🛠️ Installation & Setup (Google Colab)

To prevent dependency conflicts ("Dependency Hell") between Hugging Face, Transformers, and NumPy, this project uses a strictly locked environment.

### Step 1: Install the Locked Environment
Create a cell in your Jupyter/Colab notebook and run the following command to install perfectly synchronized libraries:
```bash
!pip install numpy==1.26.4 "huggingface_hub==0.25.2" "transformers==4.46.1" "diffusers==0.31.0" "accelerate==0.34.2" "gradio==4.44.1" peft safetensors
