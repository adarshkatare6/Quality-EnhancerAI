# Quality-EnhancerAI
This repo contains project or Computer vision that enhances lower quality images using GAN(Generative Adversarial Network) :)
An AI-powered image upscaling web application built using **ESRGAN (Enhanced Super-Resolution GAN)** and deployed on Hugging Face Spaces.
This application enhances low-resolution images by upscaling them 4× while preserving perceptual quality and fine details.

---

## Live Demo

🔗 **Link:**  
https://huggingface.co/spaces/adarsh6/Quality-EnhancerAI 

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

## Project Structure

```bash
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
```
---

## File Descriptions

### app.py
Main Flask application file.
Handles image upload,Loads model, Runs inference, Returns output image, Manages routing and download functionality

### RRDBNet_arch.py
Defines the ESRGAN model architecture.
Residual Dense Blocks, Residual-in-Residual Learning, Upsampling layers, Final reconstruction layers

### net_interp.py
Research utility script.
Performs linear interpolation between PSNR and ESRGAN pretrained weights, Used to experiment with perceptual vs distortion trade-off.

### transer_RRDB_models.py
Model conversion utility.
Cleans pretrained checkpoint keys, Maps model weights to architecture format, Used for compatibility adjustments

### templates/index.html
Frontend UI structure.Upload interface, Output display, Loader integration

### static/css/index.css
Custom styling for UI.
Responsive layout, Side-by-side input/output, Loader animation

### Procfile
Defines application start command for deployment platforms.

## 🔒 Restricted Files

The following files are not publicly uploaded due to size and licensing considerations:
- Pretrained model weights (.pth)
- Deployment-specific configuration files
- Local environment files
- Internal experimentation resources

## How It Works

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

**For restricted files contact @adarshkatare6@gmail.com**
