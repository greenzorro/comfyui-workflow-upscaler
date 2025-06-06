# comfyui-workflow-upscaler

[🇬🇧 EN](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/README.md) | [🇨🇳 中文](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/README_ZH_CN.md)

ComfyUI upscale 工作流。

## 🔍 Sharpening upscaler

[⏬ Sharpening upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.json)

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.png?raw=true)

为图像添加细节，提升分辨率。该工作流仅使用了一个upscaler模型。

## 🎨 Creative upscaler

[⏬ Creative upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.json)

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.png?raw=true)

利用 AI 想象出更多细节。输出效果更佳，但图中的元素可能会发生变化。

为潜空间图像设置了较低的denoise值，结合 ControlNet 的运用，来保持图片内容。

当效果不理想时，尝试调整ControlNet权重和denoise参数。

## 示例

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
| ComfyUI_UltimateSDUpscale    | [https://github.com/ssitu/ComfyUI_UltimateSDUpscale.git](https://github.com/ssitu/ComfyUI_UltimateSDUpscale.git)                   |
| ComfyUI-Anyline              | [https://github.com/TheMistoAI/ComfyUI-Anyline.git](https://github.com/TheMistoAI/ComfyUI-Anyline.git)                             |

### 模型

| Dir            | Model                               | Link                                                                                                                                                                                                                                         |
| -------------- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| checkpoints    | DreamShaperXL_Lightning.safetensors | [https://huggingface.co/Lykon/dreamshaper-xl-lightning/resolve/main/DreamShaperXL_Lightning.safetensors?download=true](https://huggingface.co/Lykon/dreamshaper-xl-lightning/resolve/main/DreamShaperXL_Lightning.safetensors?download=true) |
| controlnet     | mistoLine_rank256.safetensors       | [https://huggingface.co/TheMistoAI/MistoLine/resolve/main/mistoLine_rank256.safetensors?download=true](https://huggingface.co/TheMistoAI/MistoLine/resolve/main/mistoLine_rank256.safetensors?download=true)                                 |
| upscale_models | 4x-UltraSharp.pth                   | [https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true](https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true)                                                           |
| embeddings     | negativeXL_D.safetensors            | [https://civitai.com/api/download/models/134583](https://civitai.com/api/download/models/134583)                                                                                                                                             |
| loras          | add-detail-xl.safetensors           | [https://civitai.com/api/download/models/135867?type=Model&format=SafeTensor](https://civitai.com/api/download/models/135867?type=Model&format=SafeTensor)                                                                                   |

## 运行环境

除了本地运行，您还可以使用我的notebook代码在云端运行，**无需额外配置**：

- [Kaggle notebook](https://www.kaggle.com/code/victorcheng42/comfyui-cloud) 免费使用
- [Colab notebook](https://drive.google.com/file/d/1y1TeZweMvelTWZ3wBVtZuD02nLS7V8Af/view?usp=sharing) 使用更强大的 GPU（Colab付费版）

还可在 [Liblib](https://www.liblib.art/modelinfo/c9158a76d22645a19c23749b5c21dfea) 上运行。

## 感谢

特别感谢 [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler) 给我的启发！Clarity-upscaler 基于 A1111，尚未提供 ComfyUI 工作流（更新：现在有了）。我尝试了它所用的模型，捣鼓出了自己的简化替代方案。我得承认，我的工作流不如原版 clarity-upscaler 的好，但仍然管用。

---

由 [Victor_42](https://victor42.work/) 创造