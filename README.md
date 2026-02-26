# Quality-VisionAI
This repo contains project or Computer vision that enhances lower quality images using GAN(Generative Adversarial Network) :)

An AI-powered image upscaling web application built using **ESRGAN (Enhanced Super-Resolution GAN)** and deployed on Hugging Face Spaces.
This application enhances low-resolution images by upscaling them 4× while preserving perceptual quality and fine details.

---

## Live Demo

🔗 **Link:**  
https://huggingface.co/spaces/adarsh6/Quality-EnhancerAI 

---

## Project Details

This project uses:

- **RRDBNet (Residual in Residual Dense Block Network)**
- 23 RRDB Blocks
- 64 Feature Maps
- 4× Upscaling Factor
- Pretrained ESRGAN weights

Architecture components:
(Architecture code in **RRDBNet_arch.py**)
- Residual Dense Blocks
- Residual-in-Residual Learning
- Nearest-neighbor upsampling
- Final reconstruction convolution
---

## 📂 Project Structure

Quality-Enhancer/
│
├── app.py
├── RRDBNet_arch.py
├── RRDB_ESRGAN_x4.pth
├── requirements.txt
├── Dockerfile
├── README.md
│
├── static/
│ └── css/
│ └── index.css
│
└── templates/
└── index.html

---

## ⚙️ How It Works

1. User uploads an image.
2. Image is preprocessed:
   - Normalized
   - Converted to tensor
3. Passed through RRDBNet model.
4. Output tensor is:
   - Clamped
   - Converted back to image
   - Returned as Base64 for display
5. User can download enhanced image.

**For files contact @adarshkatare6@gmail.com**
