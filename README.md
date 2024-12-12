# 🎨 Text Placement Project

A Python-based project designed to add text behind the main subject of an image, offering modular and customizable solutions.

## ✨ Features

- Automatically identifies the main subject in an image.
- Places text seamlessly behind the subject.
- Command-line interface for efficient operations.
- Modular architecture for easy extension.
- Pre-trained models for subject segmentation and placement optimization.

## 📥 Installation

Steps to install and run the project:

1. Clone the repository:
   ```bash
   git clone https://github.com/rudrarathod/Video-BG-Remove.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Video-BG-Remove
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Usage

### Step 1: Prepare Your Video

Copy your video file into the main project folder.

### Step 2: Run the Functions Sequentially

Execute the following functions one by one to process your video:

1. **Convert Video to Frames** (with text and FPS):
   ```python
   video_to_frames_with_text_and_fps()
   ```
2. **Remove Background from Frames**:
   ```python
   remove_background_from_frames()
   ```
3. **Merge Images from Folders**:
   ```python
   merge_images_from_folders()
   ```
4. **Convert Frames Back to Video**:
   ```python
   frames_to_video()
   ```

### Clean Up and Setup Directories

Use the following script to reset directories:

```python
import os
import shutil

# Remove directories and their contents
shutil.rmtree('merged_frames', ignore_errors=True)
shutil.rmtree('frames', ignore_errors=True)
shutil.rmtree('frames_bgr', ignore_errors=True)
shutil.rmtree('frames_with_text', ignore_errors=True)

# Create directories if they don't exist
os.makedirs('merged_frames', exist_ok=True)
os.makedirs('frames', exist_ok=True)
os.makedirs('frames_bgr', exist_ok=True)
os.makedirs('frames_with_text', exist_ok=True)
```

## 🗂️ Project Structure

- **`code.ipynb`**: Jupyter notebook for demonstration or testing.
- **`requirements.txt`**: Lists all dependencies for the project.
- **`rembg/`**: Contains the core modules for text placement, including commands and session management.
- **`sessions/`**: Hosts various pre-trained model configurations for subject detection and text integration.

## 🤝 Contributing

Instructions to contribute to the project:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m 'Add feature-name'
   ```
4. Push to the branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

## 🙏 Acknowledgements

- [OpenCV](https://opencv.org/) for image processing tools.
- [danielgatis/rembg](https://github.com/danielgatis/rembg.git) for the image bg remove model
- Pre-trained models and datasets used for developing the sessions.
- Contributors to the open-source Python community.
