# RunPod 

Useful thinks to know

SD3 Link:
wget -P /workspace/ComfyUI/models/checkpoints --header="Authorization: Bearer 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" https://huggingface.co/stabilityai/stable-diffusion-3-medium/resolve/main/sd3_medium_incl_clips.safetensors

Make your own ANIME with this new mind-blowing AI TOOL! (ComfyUI Tutorial + FREE Workflows!)
https://www.youtube.com/watch?v=mEn3CYU7s_A

Fix Hands
https://www.youtube.com/watch?v=PLSIegjSEDg&t=12s


VAE
Add the following to /workspace/ComfyUI/models/vae
wget https://huggingface.co/stabilityai/sdxl-vae/resolve/main/sdxl_vae.safetensors


Go into the comfyUI manager, “Install models”, search for upscale and choose 4xUltrasharp. 


ControlNet
Manager > Update ComfyUi
Refresh the UI
Manager > Install Custom Nodes > Search "preprocessor" > ComfyUI's ControlNet Auxiliary Preprocessors
Manager > Install Models > Search "upscale" > 4x-Ultrasharp
Manager > Install Models > Search "upscale" > stabilityai/stable-diffusion-x4-upscaler
Manager > Install Models > Search "controlnet" > Control-LoRA: canny rank256
Manager > Install Models > Search "controlnet" > Control-LoRA: depth rank256

Alt-ControlNet
https://www.youtube.com/watch?v=UBFEw1IUX_I
cd /workspace/ComfyUI/models/controlnet;mkdir xinsir;cd xinsir
wget https://huggingface.co/xinsir/controlnet-union-sdxl-1.0/resolve/main/diffusion_pytorch_model.safetensors
Manager > Install Custom Nodes > comfyui-art-venture
wget -P /workspace/ComfyUI/models/checkpoints https://huggingface.co/RunDiffusion/Juggernaut-XL-v9/resolve/main/Juggernaut-XL_v9_RunDiffusionPhoto_v2.safetensors



Upscale
Manager > Install Custom Nodes > ComfyUI Impact Pack
Manager > Install Custom Nodes > UltimateSDUpscale
Manager > Install Custom Nodes > ComfyMath
Manager > Install Custom Nodes > Recommended Resolution Calculator
wget https://huggingface.co/FacehugmanIII/4x_foolhardy_Remacri/resolve/main/4x_foolhardy_Remacri.pth



# STS Prompts

## Jenny
raw photo, sexy 23 year old woman, brown hair, blue t-shirt, pink panties, hyper-detailed photography
raw photo, sexy 23 year old woman, brown hair, light grey t-shirt, pink panties, hyper-detailed photography, arrogant expression, smirking

## Roxxy
raw photo, sexy 18 year old girl, blonde hair, red crop-top, blue short shorts, huge tits, hyper-detailed photography, flirty eyes, licking red lollipop


New Flux model
https://www.youtube.com/watch?v=tXO6SJ-6Eb8
https://www.youtube.com/watch?v=1JtFK73K2sE - image2image
wget -P /workspace/ComfyUI/models/unet/ --header="Authorization: Bearer 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" https://huggingface.co/black-forest-labs/FLUX.1-dev/resolve/main/flux1-dev.safetensors ; wget -P /workspace/ComfyUI/models/clip/ https://huggingface.co/comfyanonymous/flux_text_encoders/resolve/main/t5xxl_fp16.safetensors ; wget -P /workspace/ComfyUI/models/clip/ https://huggingface.co/comfyanonymous/flux_text_encoders/resolve/main/clip_l.safetensors ; wget -P /workspace/ComfyUI/models/vae/ --header="Authorization: Bearer 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" https://huggingface.co/black-forest-labs/FLUX.1-dev/resolve/main/vae/diffusion_pytorch_model.safetensors
mv /workspace/ComfyUI/models/vae/diffusion_pytorch_model.safetensors /workspace/ComfyUI/models/vae/flux-dev_vae.safetensors
pip install --upgrade pip
pip install --upgrade torch torchvision torchaudio
Load workflow-flux-lam.comfyui.json


Flux with ControlNet
https://www.youtube.com/watch?v=TcQAzXjkR-c
Load: Foda-Flux-Lora-CNET-lines-v25
wget -P /workspace/ComfyUI/models/unet/ --header="Authorization: Bearer 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" https://huggingface.co/black-forest-labs/FLUX.1-dev/resolve/main/flux1-dev.safetensors ;
wget -P /workspace/ComfyUI/models/controlnet https://huggingface.co/XLabs-AI/flux-controlnet-canny-v3/resolve/main/flux-canny-controlnet-v3.safetensors ; wget -P /workspace/ComfyUI/models/controlnet https://huggingface.co/XLabs-AI/flux-controlnet-depth-v3/resolve/main/flux-depth-controlnet-v3.safetensors ; wget -P /workspace/ComfyUI/models/controlnet https://huggingface.co/XLabs-AI/flux-controlnet-hed-v3/resolve/main/flux-hed-controlnet-v3.safetensors ;
wget -P /workspace/ComfyUI/models/clip/ https://huggingface.co/comfyanonymous/flux_text_encoders/resolve/main/t5xxl_fp16.safetensors ; wget -P /workspace/ComfyUI/models/clip/ https://huggingface.co/comfyanonymous/flux_text_encoders/resolve/main/clip_l.safetensors ; 
wget -P /workspace/ComfyUI/models/vae/ --header="Authorization: Bearer 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" https://huggingface.co/black-forest-labs/FLUX.1-dev/resolve/main/vae/diffusion_pytorch_model.safetensors ; mv /workspace/ComfyUI/models/vae/diffusion_pytorch_model.safetensors /workspace/ComfyUI/models/vae/flux-dev_vae.safetensors
wget -P /workspace/ComfyUI/models/loras https://huggingface.co/XLabs-AI/flux-RealismLora/resolve/main/lora.safetensors
wget -P /workspace/ComfyUI/models/loras https://huggingface.co/XLabs-AI/flux-lora-collection/resolve/main/scenery_lora_comfy_converted.safetensors

Roxxy
Portrait of a young woman, age 18, with straight long blonde hair. She has huge, over-sized breasts. She is wearing a red crop top and light blue workout short shorts. She has a pink bracelet on her wrist. With her right hand she is touching a small pink lollipop to her lips. Her lips are slightly parted and she is smiling. The background is white, the lighting is soft and natural, creating a dreamy atmosphere. The overall mood of the image is playful and provocative.

Jenny
Portrait image of a sexy young woman standing with her arms crossed over her chest. She has huge, over-sized breasts. She is wearing a grey t-shirt and a pink underwear. Her hair is styled in loose waves and she is looking directly at the camera with a flirty, smirk. The background is a plain grey color. The woman appears to be in her early twenties.



ComfyUI with Flux.1 dev one-click
wget -P /workspace/ComfyUI/models/xlabs/controlnets/flux https://huggingface.co/XLabs-AI/flux-controlnet-canny-v3/resolve/main/flux-canny-controlnet-v3.safetensors ; wget -P /workspace/ComfyUI/models/xlabs/controlnets/flux https://huggingface.co/XLabs-AI/flux-controlnet-depth-v3/resolve/main/flux-depth-controlnet-v3.safetensors ; wget -P /workspace/ComfyUI/models/xlabs/controlnets/flux https://huggingface.co/XLabs-AI/flux-controlnet-hed-v3/resolve/main/flux-hed-controlnet-v3.safetensors ;


# Download and move t5xxl_fp16.safetensors
RUN wget -P /ComfyUI/models/clip/ https://huggingface.co/comfyanonymous/flux_text_encoders/resolve/main/t5xxl_fp16.safetensors

RUN wget -P /ComfyUI/models/controlnet https://huggingface.co/XLabs-AI/flux-controlnet-canny-v3/resolve/main/flux-canny-controlnet-v3.safetensors
RUN wget -P /ComfyUI/models/controlnet https://huggingface.co/XLabs-AI/flux-controlnet-depth-v3/resolve/main/flux-depth-controlnet-v3.safetensors
RUN wget -P /ComfyUI/models/controlnet https://huggingface.co/XLabs-AI/flux-controlnet-hed-v3/resolve/main/flux-hed-controlnet-v3.safetensors

COPY --chmod=755 controlnet.json /ComfyUI/pysssss-workflows/controlnet.json
