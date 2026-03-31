[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1TaORtSJILI4NbF8AjgJcHtFrUyHPV7c7))

⚡ Optimized Private Studio (Colab Free Edition)

A high-performance Google Colab notebook designed for private, high-quality image generation using Stable Diffusion and Wan2.1 models. This project is specifically optimized to run on the free-tier NVIDIA Tesla T4 GPU by utilizing advanced memory management and 4-bit quantization.
🚀 Key Features

    Multiple Model Presets: Built-in support for Wan2.1-T2I-1.3B, SDXL 1.0, SDXL Turbo, and DreamShaper-XL.

    VRAM Optimization: Automatically enables 4-bit quantization (via bitsandbytes), VAE tiling, VAE slicing, and sequential CPU offloading to prevent Out-of-Memory (OOM) errors on 16GB GPUs.

    Secure Access: Integrated authentication system (admin / 2025 by default) and Gradio-powered public URLs for remote access.

    Secret Management: Seamlessly connects with Google Colab userdata to securely handle Hugging Face and Civitai API tokens.

    Civitai Integration: Includes a custom ModelManager class capable of downloading models directly from Civitai via API.

🛠️ Setup Requirements

To ensure the notebook functions correctly, you must add the following Secrets to your Google Colab (click the 🔑 icon on the left):

    HF_TOKEN: Your Hugging Face Access Token (Required for gated models).

    CIVITAI_API_TOKEN: Your Civitai API Key (Optional, for downloading Civitai models).

    Ngrok: Your Ngrok Auth Token (Optional for persistent tunneling).

📖 How to Use

    Initialize Environment: Run the Setup & Security Configuration cell to install dependencies and verify your GPU.

    Launch the UI: Run the Launch Secure Optimized UI cell. You can customize the USER and PASS parameters before running.

    Load a Model: In the Gradio interface, select a model from the dropdown or enter a custom Hugging Face ID, then click Initialize Engine.

    Generate: Enter your prompt, adjust settings (steps, CFG, resolution), and click Generate.

♻️ Memory Management

If you encounter slowness or errors, the UI includes an Emergency RAM Clear button that triggers a garbage collection and clears the PyTorch CUDA cache.
