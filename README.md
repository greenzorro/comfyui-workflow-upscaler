# comfyui-workflow-upscaler

ComfyUI workflows for upscaling.

ComfyUI upscale 工作流。

## 🔍 Sharpening upscaler

[⏬ Sharpening upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.json)

Add details to an image to boost its resolution. Only one upscaler model is used in the workflow.

为图像添加细节，提升分辨率。该工作流仅使用了一个upscaler模型。

## 🎨 Creative upscaler

[⏬ Creative upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.json)

Add more details with AI imagination. The output looks better, elements in the image may vary.

Multiple LoRAs to add details. Low denoise value for latent image and ControlNet to keep the composition.

利用 AI 想象出更多细节。输出效果更佳，但图中的元素可能会发生变化。

使用了多个 LoRA 来增加细节。为潜空间图像设置了较低的denoise值，结合 ControlNet 的运用，来保持图片内容。

Source image（原图）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_source.png?raw=true)

Upscaled image（放大效果）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_creative.png?raw=true)

Source image（原图）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_2_source.png?raw=true)

Upscaled image（放大效果）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/examples/example_2_creative.png?raw=true)

When it does not work for you, try adjusting ControlNet weight and denoise.

当效果不理想时，尝试调整ControlNet权重和denoise参数。

---

Special thanks to [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler) which inspired my workflow! Clarity-upscaler is based on A1111 and has not offered ComfyUI workflow yet(update:now it has). I played with the models it uses and somehow created my own simplified alternative. I have to say that mine is not as good as the original clarity-upscaler, but it works for me.

特别感谢 [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler) 给我的启发！Clarity-upscaler 基于 A1111，尚未提供 ComfyUI 工作流（更新：现在有了）。我尝试了它所用的模型，捣鼓出了自己的简化替代方案。我得承认，我的工作流不如原版 clarity-upscaler 的好，但仍然管用。

The nodes and models you need for my workflow:

我的工作流所需的节点和模型：

- Custom node: ComfyUI_UltimateSDUpscale [https://github.com/ssitu/ComfyUI_UltimateSDUpscale](https://github.com/ssitu/ComfyUI_UltimateSDUpscale)
- Checkpoint: dreamshaper_8.safetensors [https://civitai.com/api/download/models/128713?type=Model&format=SafeTensor&size=pruned&fp=fp16](https://civitai.com/api/download/models/128713?type=Model&format=SafeTensor&size=pruned&fp=fp16)
- ControlNet: control_v11f1e_sd15_tile.pth [https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11f1e_sd15_tile.pth?download=true](https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11f1e_sd15_tile.pth?download=true)
- LoRA: more_details.safetensors [https://civitai.com/api/download/models/87153](https://civitai.com/api/download/models/87153)
- LoRA: SDXLrender_v2.0.safetensors [https://civitai.com/api/download/models/236130](https://civitai.com/api/download/models/236130)
- Upscaler: 4x-UltraSharp.pth [https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true](https://huggingface.co/philz1337x/upscaler/resolve/main/4x-UltraSharp.pth?download=true)
