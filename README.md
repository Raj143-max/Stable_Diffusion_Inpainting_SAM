# Stable_Diffusion_Inpainting_using_Segement_Anything_Model
In this project, I have used Meta’s segment-anything(https://github.com/facebookresearch/segment-anything), Hugging Face diffusers(https://github.com/huggingface/diffusers), and Gradio to create an app that can change the background, face, clothes or anything that we select. It just wants the image, selected area, and prompt. 

# Create Stable Diffusion Inpainting Pipeline
Stable Diffusion Inpainting pipeline is created using diffuser and model weights available on https://huggingface.co/stabilityai/stable-diffusion-2-inpainting. After that, it is added to "cuda" for GPU acceleration.

# Defining Image Mask and Inpainting Function
The image mask function is created using SAM Predictor. It takes an image, selected image section, and is_backgroud boolean value to create masked image and segmentation. 
After that, the inpainting function uses the Stable Diffusion Inpainting pipeline to change selected parts of the images. The pipelines require input image, masked image, segmented image, prompt text, and negative prompt text.

# Creating Gradio UI
A row and add three image blocks are created. For a minimal viable product, another row with a submit button is added. After that, we have to modify the input image object to select pixels, generate mask and segmentation, and add action to the submit button to run the inpainting function.

# Output
As you can see, the final version app looks clean with a segmentation block, clean button, background option, and negative prompt. 
![Stable_SAM_demo](https://github.com/PriyanshuSingh2002/Stable_Diffusion_Inpainting_SAM/assets/113225514/9cdfb17b-df72-44c5-925b-f88f459aa73d)

