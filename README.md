# comfyui-workflow-upscaler

[🇬🇧 EN](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/README.md) | [🇨🇳 中文](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/README_ZH_CN.md)

ComfyUI workflows for upscaling.

## Updates

- 6/30/2025 2 more upscaler workflows
- 9/21/2024 Use lora to add details
- 4/24/2024 Created
- 5/9/2024 Changed model to Dreamshaper 8
- 5/20/2024 Use Ultimate Upscaler instead of Ksampler
- 5/21/2024 Changed model to Dreamshaper XL Lightning; Use Anyline as ControlNet instead of ControlNet sd1.5 tile
- 5/22/2024 Multi-step upscaling for better result

## 🔍 Sharpening upscaler

[⏬ Sharpening upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.json)

- **Sharpness**: ⭐⭐⭐
- **Creativity**: ⭐
- **Cost**: ⭐

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.png?raw=true)

Add details to an image to boost its resolution. Only one upscaler model is used. No diffusion model.

## 🎨 Creative upscaler

[⏬ Creative upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.json)

- **Sharpness**: ⭐⭐
- **Creativity**: ⭐⭐⭐⭐⭐
- **Cost**: ⭐⭐

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.png?raw=true)

Add more details with AI imagination with SDXL. Elements in the image may vary.

Low denoise value for latent image and ControlNet to keep the composition. Adjust ControlNet weight and denoise when it fails.

## 🔭 Ultra sharp upscaler

[🔭 Ultra sharp upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-ultra-sharp.json)

- **Sharpness**: ⭐⭐⭐⭐⭐
- **Creativity**: ⭐⭐⭐
- **Cost**: ⭐⭐⭐

Significantly boost an image by resolution with Flux dev. Fails on extremely low-res images (looks pixelated).

## 💣 Mad mode upscaler

[💣 Mad mode upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-mad-mode.json)

- **Sharpness**: ⭐⭐⭐⭐⭐
- **Creativity**: ⭐⭐⭐⭐⭐
- **Cost**: ⭐⭐⭐⭐⭐

Simply stitch **🔭 Ultra sharp** to **🎨 Creative**, combining the creativity of SDXL and the hi-res of Flux dev. Can be unstable, but surprises sometimes.

## Examples (🎨 Creative)

Source image:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_source.png?raw=true)

Upscaled image:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_creative.png?raw=true)

Source image:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_2_source.png?raw=true)

Upscaled image:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_2_creative.png?raw=true)

## Prerequisite

### Custom nodes

| Node                         | Link                                                                                                                               |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| ComfyUI_Essentials           | [https://github.com/cubiq/ComfyUI_essentials.git](https://github.com/cubiq/ComfyUI_essentials.git)                                 |
| ComfyUI-Easy-Use             | [https://github.com/yolain/ComfyUI-Easy-Use.git](https://github.com/yolain/ComfyUI-Easy-Use.git)                                   |
| ComfyUI-Anyline              | [https://github.com/TheMistoAI/ComfyUI-Anyline.git](https://github.com/TheMistoAI/ComfyUI-Anyline.git)                             |
| ComfyUI_UltimateSDUpscale    | [https://github.com/ssitu/ComfyUI_UltimateSDUpscale.git](https://github.com/ssitu/ComfyUI_UltimateSDUpscale.git)                   |
| Comfyui_TTP_Toolset          | [https://github.com/TTPlanetPig/Comfyui_TTP_Toolset.git](https://github.com/TTPlanetPig/Comfyui_TTP_Toolset.git)                   |

### Models

| Dir            | Model                               | Link                                                                                                                                                                                                                                         |
| -------------- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| unet           | flux1-dev.safetensors               | [https://huggingface.co/black-forest-labs/FLUX.1-dev/resolve/main/flux1-dev.safetensors?download=true](https://huggingface.co/black-forest-labs/FLUX.1-dev/resolve/main/flux1-dev.safetensors?download=true)                             |
| checkpoints    | DreamShaperXL_Lightning.safetensors | [https://huggingface.co/Lykon/dreamshaper-xl-lightning/resolve/main/DreamShaperXL_Lightning.safetensors?download=true](https://huggingface.co/Lykon/dreamshaper-xl-lightning/resolve/main/DreamShaperXL_Lightning.safetensors?download=true) |
| clip           | clip_l.safetensors                  | [https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/resolve/main/text_encoders/clip_l.safetensors?download=true](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/resolve/main/text_encoders/clip_l.safetensors?download=true) |
| clip           | t5xxl_fp8_e4m3fn.safetensors        | [https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/resolve/main/text_encoders/t5xxl_fp8_e4m3fn.safetensors?download=true](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/resolve/main/text_encoders/t5xxl_fp8_e4m3fn.safetensors?download=true) |
| vae            | flux-ae.safetensors                 | [https://huggingface.co/black-forest-labs/FLUX.1-dev/resolve/main/flux-ae.safetensors](https://huggingface.co/black-forest-labs/FLUX.1-dev/resolve/main/flux-ae.safetensors)                                                               |
| controlnet     | mistoLine_rank256.safetensors       | [https://huggingface.co/TheMistoAI/MistoLine/resolve/main/mistoLine_rank256.safetensors?download=true](https://huggingface.co/TheMistoAI/MistoLine/resolve/main/mistoLine_rank256.safetensors?download=true)                                 |
| upscale_models | 4x-UltraSharp.pth                   | [https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true](https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true)                                                           |
| upscale_models | 4x_NMKD-Siax_200k.pth               | [https://huggingface.co/uwg/upscaler/resolve/main/ESRGAN/4x_NMKD-Siax_200k.pth?download=true](https://huggingface.co/uwg/upscaler/resolve/main/ESRGAN/4x_NMKD-Siax_200k.pth?download=true)                                                 |
| embeddings     | negativeXL_D.safetensors            | [https://civitai.com/api/download/models/134583](https://civitai.com/api/download/models/134583)                                                                                                                                             |
| loras          | add-detail-xl.safetensors           | [https://civitai.com/api/download/models/135867?type=Model&format=SafeTensor](https://civitai.com/api/download/models/135867?type=Model&format=SafeTensor)                                                                                   |
| loras          | Flux Dev模型4步出图lora             | [https://www.liblib.art/modelinfo/466cd07b9c9248369e236fd2b1a90414](https://www.liblib.art/modelinfo/466cd07b9c9248369e236fd2b1a90414)                                                                                                       |

## Where to run?

Besides running locally, you may run them on the cloud **without extra configuration**, using my notebook code:

- [Kaggle notebook](https://www.kaggle.com/code/victorcheng42/comfyui-cloud) for free
- [Colab notebook](https://drive.google.com/file/d/1y1TeZweMvelTWZ3wBVtZuD02nLS7V8Af/view?usp=sharing) for more powerful GPUs (Colab paid plan needed)

## Thanks

Special thanks to [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler) which inspired my workflow! Clarity-upscaler is based on A1111 and has not offered ComfyUI workflow yet(update:now it has). I played with the models it uses and somehow created my own simplified alternative. I have to say that mine is not as good as the original clarity-upscaler, but it works for me.

---

Created by [Victor42](https://victor42.work/)
