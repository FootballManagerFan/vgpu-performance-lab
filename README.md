# vgpu-performance-lab

comparing AI workloads on nvidia gpu models in a cloud based setting. Hope to compare to local ROM/CUDA enviroments. 

- using google colab for gpu power

# Setup
# Install Python 3.10 and set it as the default
!sudo apt-get update -y
!sudo apt-get install python3.10
!sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.10 1

# Verify the Python version
!python3 --version

# --- The rest of the original script ---

# Clone the Automatic1111 repository
!git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui
%cd stable-diffusion-webui

# Download a model to use
!wget -q https://huggingface.co/stabilityai/stable-diffusion-2-1-base/resolve/main/v2-1-base-ema.ckpt -O /content/stable-diffusion-webui/models/Stable-diffusion/v2-1-base-ema.ckpt

# Launch the web UI with a shareable link
!python launch.py --share --enable-insecure-extension-access
