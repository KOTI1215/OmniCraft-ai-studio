# OmniCraft AI Studio 🚀
> Dual-Stage Visual Synthesis & Typography Protection Pipeline for Commercial E-Commerce Listings.

[![Live Demo](https://img.shields.io/badge/Live_Demo-Render-blue?style=flat-square)](https://omnicraft-ai-studio.onrender.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg?style=flat-square)](https://opensource.org/licenses/MIT)

## 📌 Overview
OmniCraft AI Studio bridges the gap between raw smartphone product photography and studio-grade commercial catalog assets. By decoupling alpha matting from diffusion inpainting, it prevents text hallucination and maintains 100% brand typography fidelity.

## 🛠️ Architecture & Pipeline
1. **Foreground Isolation**: `u2netp` generates high-resolution alpha mattes directly from raw image inputs.
2. **Typography Protection**: Generates an inverted binary mask ($0$ on foreground product & branding; $255$ on background context).
3. **Latent Inpainting**: Guided generative synthesis using `runwayml/stable-diffusion-inpainting` with attention slicing enabled for edge-efficient T4 GPU inference.
4. **Decoupled Architecture**: Google Colab backend server tunneled via Gradio, embedded seamlessly inside a responsive Tailwind CSS frontend deployed on Render.

## 💻 Tech Stack
- **Deep Learning / CV**: PyTorch, Hugging Face Diffusers, `rembg`, ONNX Runtime
- **Backend / Serving**: Gradio Live Tunnel, Google Colab (T4 GPU runtime)
- **Frontend / Deployment**: Tailwind CSS, HTML5, Render Static Sites

## 🌐 Live Access
- **Frontend**: [omnicraft-ai-studio.onrender.com](https://omnicraft-ai-studio.onrender.com)
-
