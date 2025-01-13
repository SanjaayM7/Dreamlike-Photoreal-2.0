# Dreamlike Photoreal 2.0

## Overview

This repository contains the model **Dreamlike Photoreal 2.0** which specializes in generating photorealistic images from text descriptions. It is optimized for producing lifelike images that closely resemble real-world photos. Whether you are creating realistic landscapes, portraits, or objects, this model produces impressive results.

## Features

- **Photorealistic Image Generation**: Focuses on highly realistic and accurate image generation.
- **Versatile for Real-World Scenes**: Ideal for generating realistic images of people, objects, or nature.
- **Optimized for Detail**: Generates fine details with photorealistic textures and lighting.

## Installation

Dreamlike Photoreal 2.0 can be run in Google Colab for ease of use or locally if you set up the environment correctly.

### Prerequisites

- **Google Colab (Recommended)**: Run the model on Colab using GPU acceleration.
- **Hugging Face Account**: Some models require authentication. Generate a Hugging Face token [here](https://huggingface.co/settings/tokens).

### Setup in Google Colab

1. **Open Google Colab** and create a new notebook.
2. **Install the required dependencies**:
    ```python
    !pip install diffusers transformers accelerate torch torchvision pillow
    ```

3. **Load the Dreamlike Photoreal 2.0 model** and generate images:

    ```python
    from diffusers import StableDiffusionPipeline

    # Load the model from Hugging Face
    model_id = "dreamlike-art/dreamlike-photoreal-2.0"
    pipe = StableDiffusionPipeline.from_pretrained(model_id)

    # Example prompt
    prompt = "A hyper-realistic portrait of a smiling elderly woman"

    # Generate image
    image = pipe(prompt).images[0]
    image.show()
    ```

### Example Usage

You can modify the prompt to generate different types of photorealistic images:

```python
prompt = "A serene forest with morning sunlight streaming through the trees"
image = pipe(prompt).images[0]
image.show()
