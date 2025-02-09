# Image-generation-using-ComfyUI-and-stable-diffusion
This document details my AICTE internship project on AI, part of the Transformative Learning with TechSaksham program, a joint CSR initiative of Microsoft and SAP.  The project utilizes Stable Diffusion and ComfyUI to generate images from text prompts. ComfyUI's node-based interface simplifies and enhances control over Stable Diffusion's image generation capabilities.

**Contents:**

*   Introduction
*   Features
*   Requirements
*   Installation
*   Usage

**Introduction:**

This project leverages Stable Diffusion, a powerful deep learning model for high-quality text-to-image synthesis.  ComfyUI provides a visual programming environment, enabling users to create custom image generation pipelines and interact more effectively with Stable Diffusion.  The combination of these tools results in a user-friendly and highly customizable image generation experience.

**Features:**

*   **Visual Workflow Design:** Construct complex image generation pipelines using ComfyUI's node-based system.
*   **Text-to-Image Generation:** Generate images from text descriptions using Stable Diffusion.
*   **Customizable Parameters:** Fine-tune image generation parameters within ComfyUI for specific artistic styles and results.
*   **Modular Design:** Easily modify image processing techniques by adding, removing, or rearranging ComfyUI nodes.
*   **Real-time Feedback:** (Potentially, depending on ComfyUI features) Preview generated images as parameters are adjusted, streamlining the creative process.
*   **Extensible with Custom Scripts:** Integrate custom Python scripts and nodes into ComfyUI for advanced functionalities.

**Requirements:**

**Hardware:**

*   **Operating System:** Windows 10/11, macOS, or Linux (Linux recommended for optimal performance).
*   **CPU:** Modern multi-core processor.
*   **GPU:** NVIDIA GPU with at least 8GB VRAM (12GB+ recommended). AMD GPUs are supported but may require specific configurations and may exhibit lower performance.
*   **RAM:** 16GB minimum (32GB+ recommended).
*   **Storage:** Fast SSD with ample space.

**Software:**

*   **Python:** 3.8+ (3.10 or 3.11 recommended).
*   **ComfyUI:** Download and install from the official repository.
*   **Stable Diffusion Model Checkpoint:** Download a compatible model file (e.g., `.ckpt` or `.safetensors`).
*   **Python Libraries (install via `pip`):**
    *   `torch torchvision torchaudio` (for PyTorch)
    *   `transformers`
    *   `numpy`
    *   `Pillow`
    *   `Flask` (for web interface)
    *   `requests`
    *   `tqdm`
    *   `filelock`
    *   `gradio` (for Gradio interface)
    *   `omegaconf`

**Installation:**

1.  **Install Python:** Ensure Python 3.8 or higher is installed (3.10 or 3.11 recommended).

2.  **Install ComfyUI:** ComfyUI was deployed locally from the GitHub repository (provide link if available). Follow the repository's setup instructions.

3.  **Download Stable Diffusion Model:** The v1-5-pruned-emaonly-fp16 model was downloaded from Hugging Face (provide link if possible).

4.  **Place Model Checkpoint:** Place the downloaded model file (v1-5-pruned-emaonly-fp16) in the `ComfyUI_windows_portable\ComfyUI\models\checkpoints` directory within your ComfyUI installation. This is the designated location for model files.

5.  **Install Dependencies:** Open a terminal in your ComfyUI directory and create a virtual environment (recommended):

    ```bash
    python3 -m venv .venv        # Create virtual environment
    source .venv/bin/activate    # Activate (Linux/macOS)
    .venv\Scripts\activate      # Activate (Windows)
    ```

    Then, install the required libraries:

    ```bash
    pip install torch torchvision torchaudio transformers numpy Pillow Flask requests tqdm filelock gradio omegaconf
    ```

    (Important: Ensure PyTorch installation matches your CUDA version if you have a compatible NVIDIA GPU. Consult PyTorch installation instructions for specific CUDA versions.)

6.  **Run ComfyUI:** Launch ComfyUI as per its documentation.  ComfyUI should automatically detect the model checkpoint in the correct directory upon startup.

**Usage:**

1.  **Run ComfyUI:** Launch ComfyUI.
2.  **Load Workflow (Optional):** Load a pre-designed ComfyUI workflow or create a new one.
3.  **Input Prompt:** Enter your text prompt in the designated ComfyUI node.
4.  **Adjust Parameters:** Modify node parameters to customize image generation.
5.  **Generate Image:** Execute the workflow.
6.  **View Results:** The generated image will be displayed in ComfyUI.
