# 🧠 Prompt-Based Image Generation with Diffusion Models

This project allows users to generate high-quality images from text prompts using a diffusion-based model pipeline (such as Stable Diffusion). Built in Google Colab with interactive UI elements using `ipywidgets`, it enables real-time image generation and download functionality.

---

## 📌 Features

- 🔤 Enter custom text prompts via input box  
- 🧠 Generate realistic images using a pretrained model  
- 🖼️ View the generated image inline  
- 💾 Save & download images automatically  
- 🧰 Built with PyTorch, Matplotlib, HuggingFace Diffusers, and Google Colab widgets  

---

## 📂 Project Structure

```
📁 /content/images/     # Folder where images are saved
📄 README.md            # Project description
📄 main.ipynb           # Google Colab notebook with full code
```

---

## ⚙️ Setup Instructions

1. Open the Colab notebook.
2. Install required packages:
   ```python
   !pip install diffusers transformers ipywidgets torch
   ```
3. Authenticate with HuggingFace if needed:
   ```python
   from huggingface_hub import notebook_login
   notebook_login()
   ```
4. Load the pipeline:
   ```python
   from diffusers import StableDiffusionPipeline
   pipe = StableDiffusionPipeline.from_pretrained("CompVis/stable-diffusion-v1-4", torch_dtype=torch.float16)
   pipe = pipe.to("cuda")
   ```

---

## 🚀 Usage

1. Enter a prompt in the text field (e.g., `"a futuristic city at night"`).
2. Click the **Generate Image** button.
3. The image will be:
   - Displayed in the output
   - Saved to `/content/images/`
   - Automatically downloaded

---

## 📷 Example

| Prompt | Output |
|--------|--------|
| *a castle on a mountain during sunset* | ![Example Image](images/example_image.png) |

---

## 🧩 Dependencies

- `torch`
- `diffusers`
- `ipywidgets`
- `matplotlib`
- `transformers`

---

## 📜 License

This project is for educational purposes only. Respect the licensing terms of the models used (e.g., Stable Diffusion).