# comfyui-workflow-upscaler

[🇬🇧 EN](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/README.md) | [🇨🇳 中文](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/README_ZH_CN.md)

ComfyUI workflows for upscaling.

## Updates

- 9/21/2024 Use lora to add details
- 4/24/2024 Created
- 5/9/2024 Changed model to Dreamshaper 8
- 5/20/2024 Use Ultimate Upscaler instead of Ksampler
- 5/21/2024 Changed model to Dreamshaper XL Lightning; Use Anyline as ControlNet instead of ControlNet sd1.5 tile
- 5/22/2024 Multi-step upscaling for better result

## 🔍 Sharpening upscaler

[⏬ Sharpening upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.json)

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.png?raw=true)

Add details to an image to boost its resolution. Only one upscaler model is used in the workflow.

## 🎨 Creative upscaler

[⏬ Creative upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.json)

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.png?raw=true)

Add more details with AI imagination. The output looks better, elements in the image may vary.

Low denoise value for latent image and ControlNet to keep the composition.

When it does not work for you, try adjusting ControlNet weight and denoise.

## Examples

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
| ComfyUI_UltimateSDUpscale    | [https://github.com/ssitu/ComfyUI_UltimateSDUpscale.git](https://github.com/ssitu/ComfyUI_UltimateSDUpscale.git)                   |
| ComfyUI-Anyline              | [https://github.com/TheMistoAI/ComfyUI-Anyline.git](https://github.com/TheMistoAI/ComfyUI-Anyline.git)                             |

### Models

| Dir            | Model                               | Link                                                                                                                                                                                                                                         |
| -------------- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| checkpoints    | DreamShaperXL_Lightning.safetensors | [https://huggingface.co/Lykon/dreamshaper-xl-lightning/resolve/main/DreamShaperXL_Lightning.safetensors?download=true](https://huggingface.co/Lykon/dreamshaper-xl-lightning/resolve/main/DreamShaperXL_Lightning.safetensors?download=true) |
| controlnet     | mistoLine_rank256.safetensors       | [https://huggingface.co/TheMistoAI/MistoLine/resolve/main/mistoLine_rank256.safetensors?download=true](https://huggingface.co/TheMistoAI/MistoLine/resolve/main/mistoLine_rank256.safetensors?download=true)                                 |
| upscale_models | 4x-UltraSharp.pth                   | [https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true](https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true)                                                           |
| embeddings     | negativeXL_D.safetensors            | [https://civitai.com/api/download/models/134583](https://civitai.com/api/download/models/134583)                                                                                                                                             |
| loras          | add-detail-xl.safetensors           | [https://civitai.com/api/download/models/135867?type=Model&format=SafeTensor](https://civitai.com/api/download/models/135867?type=Model&format=SafeTensor)                                                                                   |

## Where to run?

Besides running locally, you may run them on the cloud **without extra configuration**, using my notebook code:

- [Kaggle notebook](https://www.kaggle.com/code/victorcheng42/comfyui-cloud) for free
- [Colab notebook](https://drive.google.com/file/d/1y1TeZweMvelTWZ3wBVtZuD02nLS7V8Af/view?usp=sharing) for more powerful GPUs (Colab paid plan needed)

## Thanks

Special thanks to [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler) which inspired my workflow! Clarity-upscaler is based on A1111 and has not offered ComfyUI workflow yet(update:now it has). I played with the models it uses and somehow created my own simplified alternative. I have to say that mine is not as good as the original clarity-upscaler, but it works for me.

---

Created by [Victor_42](https://victor42.work/)