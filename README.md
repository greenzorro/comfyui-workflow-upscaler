# comfyui-workflow-upscaler
ComfyUI workflows for upscaling.

用于提升分辨率的 ComfyUI 工作流。

## Sharpening upscaler

[Sharpening upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.json)

Add details to an image to boost its resolution. Only one upscaler model is used in the workflow.

为图像添加细节以提高其分辨率。该工作流仅使用了一个upscaler模型。

## Creative upscaler

[Creative upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.json)

Add more details with AI imagination. The output looks better, elements in the image may vary.
Multiple LoRAs to add details. Low denoise value for latent image and ControlNet to keep the composition.

利用 AI 想象更多细节。输出效果更佳，但图像中的元素可能会发生变化。
使用了多个 LoRA 来添加细节。为潜空间图像设置较低的denoise值，以及运用 ControlNet 来保持图片内容构成。

Source image（原图）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/example_source.png?raw=true)

Upscaled image（放大效果）:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/example_creative.png?raw=true)

---

Special thanks to [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler)! It does not offer ComfyUI workflow yet. I played with the models from it and created my own simplified ComfyUI alternative.

特别感谢 [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler)！它尚未提供 ComfyUI 工作流。我使用了它的模型并创建了我自己的简易 ComfyUI 版本。
