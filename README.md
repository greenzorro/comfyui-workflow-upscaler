# comfyui-workflow-upscaler

ComfyUI workflows for upscaling.

ComfyUI upscale 工作流。

## Updates 更新记录

- 4/24/2024 Created
- 5/9/2024 Changed model to Dreamshaper 8
- 5/20/2024 Use Ultimate Upscaler instead of Ksampler
- 5/21/2024 Changed model to Dreamshaper XL Lightning; Use Anyline as ControlNet instead of ControlNet sd1.5 tile
- 5/22/2024 Multi-step upscaling for better result

## 🔍 Sharpening upscaler

[⏬ Sharpening upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.json)

Add details to an image to boost its resolution. Only one upscaler model is used in the workflow.

为图像添加细节，提升分辨率。该工作流仅使用了一个upscaler模型。

## 🎨 Creative upscaler

[⏬ Creative upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.json)

Add more details with AI imagination. The output looks better, elements in the image may vary.

Low denoise value for latent image and ControlNet to keep the composition.

When it does not work for you, try adjusting ControlNet weight and denoise.

利用 AI 想象出更多细节。输出效果更佳，但图中的元素可能会发生变化。

为潜空间图像设置了较低的denoise值，结合 ControlNet 的运用，来保持图片内容。

当效果不理想时，尝试调整ControlNet权重和denoise参数。

## Examples 示例

Source image（原图）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_source.png?raw=true)

Upscaled image（放大效果）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_creative.png?raw=true)

Source image（原图）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_2_source.png?raw=true)

Upscaled image（放大效果）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_2_creative.png?raw=true)

## Prerequisite 使用前提

The nodes and models you need for my workflow:

我的工作流所需的节点和模型：

- Custom node: ComfyUI_UltimateSDUpscale [https://github.com/ssitu/ComfyUI_UltimateSDUpscale](https://github.com/ssitu/ComfyUI_UltimateSDUpscale)
- Custom node: ComfyUI-Anyline [https://github.com/TheMistoAI/ComfyUI-Anyline.git](https://github.com/TheMistoAI/ComfyUI-Anyline.git)
- Checkpoint: DreamShaperXL_Lightning.safetensors [https://huggingface.co/Lykon/dreamshaper-xl-lightning/resolve/main/DreamShaperXL_Lightning.safetensors?download=true](https://huggingface.co/Lykon/dreamshaper-xl-lightning/resolve/main/DreamShaperXL_Lightning.safetensors?download=true)
- ControlNet: mistoLine_rank256.safetensors [https://huggingface.co/TheMistoAI/MistoLine/resolve/main/mistoLine_rank256.safetensors?download=true](https://huggingface.co/TheMistoAI/MistoLine/resolve/main/mistoLine_rank256.safetensors?download=true)
- Upscaler: 4x-UltraSharp.pth [https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true](https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true)
- Embedding: negativeXL_D.safetensors [https://civitai.com/api/download/models/134583](https://civitai.com/api/download/models/134583)

## Citation 感谢

Special thanks to [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler) which inspired my workflow! Clarity-upscaler is based on A1111 and has not offered ComfyUI workflow yet(update:now it has). I played with the models it uses and somehow created my own simplified alternative. I have to say that mine is not as good as the original clarity-upscaler, but it works for me.

特别感谢 [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler) 给我的启发！Clarity-upscaler 基于 A1111，尚未提供 ComfyUI 工作流（更新：现在有了）。我尝试了它所用的模型，捣鼓出了自己的简化替代方案。我得承认，我的工作流不如原版 clarity-upscaler 的好，但仍然管用。

AUTOMATIC1111. (2022). Stable Diffusion Web UI [Computer software]. https://github.com/AUTOMATIC1111/stable-diffusion-webui
