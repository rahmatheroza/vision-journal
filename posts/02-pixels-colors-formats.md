# 🧠 Week 2 – Pixels, Colors, and Formats

## 👋 Introduction

To humans, an image is a photo or a scene. To a computer? It's just numbers.

In this post, we’ll explore how digital images are stored and processed by machines. You’ll learn:
- What pixels really are
- How colors are represented
- Why image formats like JPEG and PNG matter

Let’s break it down.

---

## 🟨 1. What is a Digital Image?

A digital image is made of tiny squares called **pixels** — think of them like colored tiles.

- **Grayscale image** → A 2D array (matrix) of pixel values  
  - Each value represents brightness (0 = black, 255 = white)
- **Color image** → A 3D array  
  - Each pixel is made of 3 values: **Red**, **Green**, and **Blue**

```python
# Example with OpenCV
import cv2
img = cv2.imread('dog.jpg')
print(img.shape)  # (height, width, 3)
```
Each number in that matrix affects how an image looks on screen.

---
## 🌈 2. Understanding RGB Channels
Color images use the **RGB model**:

- Each pixel = [Red, Green, Blue] values
- These values mix to form color, like paint
You can split and visualize them using OpenCV or matplotlib.

```python
r, g, b = cv2.split(img)
```

Try displaying each one as a grayscale image to “see like a machine.”

---
## 📁 3. Image Formats: JPEG vs PNG vs BMP
Not all images are stored the same way. Different formats serve different purposes:

| Format   | Features                        | Good For                      |
| -------- | ------------------------------- | ----------------------------- |
| **JPEG** | Lossy compression, small size   | Photos, websites              |
| **PNG**  | Lossless, supports transparency | UI assets, clean logos        |
| **BMP**  | Uncompressed, very large        | Raw image data for processing |

---

## 🚀 4. Hands-On Practice
👉 [Click here to open the notebook on Google Colab](https://github.com/rahmatheroza/vision-journal/blob/main/notebooks/02-pixels-colors-formats.ipynb)


---
