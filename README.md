# comfyui-workflow-upscaler
ComfyUI workflows for upscaling.

## Sharpening upscaler

[Sharpening upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-sharpen.json))

Add details to an image to boost its resolution.
Only one upscale model is used in the workflow.

## Creative upscaler

[Creative upscaler](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/upscaler-creative.json)

Add more details with AI imagination. The output, elements in the image may vary.
Multiple LoRAs to add details. Low denoise value for latent image and ControlNet to keep the composition.

Source image:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/example_source.png?raw=true)

Upscaled image:

![](https://github.com/greenzorro/comfyui-workflow-upscaler/blob/main/example_creative.png?raw=true)

---

Special thanks to [clarity-upscaler](https://github.com/philz1337x/clarity-upscaler)! It does not offer ComfyUI workflow yet. I played with the models from it and created my own simplified ComfyUI alternative.
