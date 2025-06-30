# comfyui-workflow-upscaler

[🇬🇧 EN](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/README.md) | [🇨🇳 中文](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/README_ZH_CN.md)

ComfyUI upscale 工作流。

## 更新日志

- 6/30/2025 新增2个放大工作流
- 9/21/2024 使用lora来增加细节
- 4/24/2024 创建
- 5/9/2024 模型修改为 Dreamshaper 8
- 5/20/2024 使用 Ultimate Upscaler 替代 Ksampler
- 5/21/2024 模型修改为 Dreamshaper XL Lightning; 使用 Anyline 替代 ControlNet sd1.5 tile
- 5/22/2024 多重放大来获得更好效果

## 🔍 Sharpening upscaler

[⏬ Sharpening upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.json)

- **清晰度**: ⭐⭐⭐
- **创意度**: ⭐
- **性能开销**: ⭐

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.png?raw=true)

为图像添加细节，提升分辨率。该工作流仅使用了一个放大模型，无扩散模型。

## 🎨 Creative upscaler

[⏬ Creative upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.json)

- **清晰度**: ⭐⭐
- **创意度**: ⭐⭐⭐⭐⭐
- **性能开销**: ⭐⭐

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.png?raw=true)

利用 AI（SDXL）想象出更多细节。图中的元素可能会发生变化。

为潜空间图像设置了较低的denoise值，结合 ControlNet 的运用，来保持图片内容。当效果不理想时，尝试调整ControlNet权重和denoise参数。

## 🔭 Ultra sharp upscaler

[🔭 Ultra sharp upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-ultra-sharp.json)

- **清晰度**: ⭐⭐⭐⭐⭐
- **创意度**: ⭐⭐⭐
- **性能开销**: ⭐⭐⭐

使用 Flux dev 来显著提升图片分辨率。在处理极低分辨率图片时会失败（图像看起来有像素感）。

## 💣 Mad mode upscaler

[💣 Mad mode upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-mad-mode.json)

- **清晰度**: ⭐⭐⭐⭐⭐
- **创意度**: ⭐⭐⭐⭐⭐
- **性能开销**: ⭐⭐⭐⭐⭐

简单地将 **🔭 Ultra sharp** 和 **🎨 Creative** 工作流连接起来，结合了 SDXL 的创意和 Flux dev 的高分辨率。该流程可能不稳定，但有时会带来惊喜。

## 示例 (🎨 Creative)

原图:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_source.png?raw=true)

放大效果:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_creative.png?raw=true)

原图:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_2_source.png?raw=true)

放大效果:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_2_creative.png?raw=true)

## 使用前提

### 节点

| Node                         | Link                                                                                                                               |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| ComfyUI_Essentials           | [https://github.com/cubiq/ComfyUI_essentials.git](https://github.com/cubiq/ComfyUI_essentials.git)                                 |
| ComfyUI-Easy-Use             | [https://github.com/yolain/ComfyUI-Easy-Use.git](https://github.com/yolain/ComfyUI-Easy-Use.git)                                   |
| ComfyUI-Anyline              | [https://github.com/TheMistoAI/ComfyUI-Anyline.git](https://github.com/TheMistoAI/ComfyUI-Anyline.git)                             |
| ComfyUI_UltimateSDUpscale    | [https://github.com/ssitu/ComfyUI_UltimateSDUpscale.git](https://github.com/ssitu/ComfyUI_UltimateSDUpscale.git)                   |
| Comfyui_TTP_Toolset          | [https://github.com/TTPlanetPig/Comfyui_TTP_Toolset.git](https://github.com/TTPlanetPig/Comfyui_TTP_Toolset.git)                   |

### 模型

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

## 运行环境

除了本地运行，您还可以使用我的notebook代码在云端运行，**无需额外配置**：

- [Kaggle notebook](https://www.kaggle.com/code/victorcheng42/comfyui-cloud) 免费使用
- [Colab notebook](https://drive.google.com/file/d/1y1TeZweMvelTWZ3wBVtZuD02nLS7V8Af/view?usp=sharing) 使用更强大的 GPU（Colab付费版）

还可在 [Liblib](https://www.liblib.art/modelinfo/c9158a76d22645a19c23749b5c21dfea) 上运行。

## 感谢

特别感谢 [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler) 给我的启发！Clarity-upscaler 基于 A1111，尚未提供 ComfyUI 工作流（更新：现在有了）。我尝试了它所用的模型，捣鼓出了自己的简化替代方案。我得承认，我的工作流不如原版 clarity-upscaler 的好，但仍然管用。

---

由 [Victor_42](https://victor42.work/) 创造