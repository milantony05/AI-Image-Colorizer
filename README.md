# AI Image Colorizer 🎨

**Automatically colorize black & white images using deep learning and OpenCV.**

![Animation](https://github.com/user-attachments/assets/7e07c542-4893-482a-b058-e7b7fcd1024a)

---

## Project Summary

This project provides a pipeline for transforming grayscale (black and white) images into vivid, plausible color photos using a deep learning model and OpenCV. It leverages a pre-trained Caffe colorization model, making it easy for anyone to enhance old photos, art, or any single-channel imagery with natural-looking color.

---

## Features

- ⚡️ **Automatic Colorization:** Converts grayscale images to color in seconds.
- 🧠 **Deep Learning:** Utilizes a robust CNN trained on ImageNet.
- 🌈 **Lab Color Space:** Achieves natural results with better separation of lightness and color.
- 🖼 **Sample Notebook:** Step-by-step Jupyter notebook included.
- 🖥 **Simple GUI:** User-friendly desktop interface (Tkinter) for non-technical users.
- 🛠 **Open Source:** Fully transparent and extensible.

---

## How It Works

1. **Input:** Provide a black & white (grayscale) image.
2. **Lab Conversion:** Image is converted to Lab color space; the model uses the 'L' channel as input.
3. **Prediction:** The model predicts the missing 'a' and 'b' color channels.
4. **Merging:** Output channels are merged back and converted to BGR/RGB.
5. **Result:** Colorized image is saved and can be visually compared to the input.

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/milantony05/AI-Image-Colorizer.git
cd AI-Image-Colorizer
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```
_You will need:_  
- Python 3.6+  
- opencv-python  
- numpy  
- matplotlib  
- pillow  
- tkinter (optional; included with standard Python installations)

### 3. Download Pretrained Models

Run these commands inside the project folder:

```bash
mkdir models
wget https://raw.githubusercontent.com/richzhang/colorization/caffe/colorization/resources/pts_in_hull.npy -O ./pts_in_hull.npy
wget https://raw.githubusercontent.com/richzhang/colorization/caffe/colorization/models/colorization_deploy_v2.prototxt -O ./models/colorization_deploy_v2.prototxt
wget https://eecs.berkeley.edu/~rich.zhang/projects/2016_colorization/files/demo_v2/colorization_release_v2.caffemodel -O ./models/colorization_release_v2.caffemodel
```

### 4. Run the Jupyter Notebook

Open [Colorize_Black_and_White_Image.ipynb](Colorize_Black_and_White_Image.ipynb) and follow the step-by-step instructions to colorize your own images.

### 5. (Optional) Use the GUI

You can launch a simple GUI to colorize images using `gui.py`:

```bash
python gui.py
```

---

## Demo example

![input](https://github.com/user-attachments/assets/30874300-70ae-451b-8a37-24936b66de54)

![output](https://github.com/user-attachments/assets/5d1ec791-9ff5-40c9-aa59-f7c0945b2a3f)

---

## References

- **Model:** Zhang, R., Isola, P., & Efros, A.A. (2016). [Colorful Image Colorization](https://richzhang.github.io/colorization/) (ECCV).
- **Code Base:** [Berkeley Colorization Models](https://github.com/richzhang/colorization)
- **OpenCV DNN Documentation:** https://docs.opencv.org/master/d6/d0f/group__dnn.html
- **ImageNet Dataset:** https://image-net.org/

---

## Acknowledgements

- Based on the pioneering work by [Richard Zhang et al.](https://richzhang.github.io/colorization/)
- Pretrained models provided under the Berkeley license.
