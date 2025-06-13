# 🧰 Week 3 – Getting Hands-On with Images in OpenCV

## 👋 Introduction

Last week, we looked at how images are stored as pixel arrays and how RGB channels work.

This week, we’ll manipulate those images using one of the most popular computer vision libraries: **OpenCV**.

You’ll learn to:
- Resize and crop images
- Rotate and flip them
- Convert to grayscale
- Apply basic filters like blur
- Draw shapes and text on an image

Let’s build your first image processing toolbox!

---

## ✂️ 1. Resize and Crop

### 🔹 Resize

Changing image size is useful when:
- Standardizing input for ML models
- Reducing memory usage

```python
resized = cv2.resize(img, (width, height))
```

Tip: Resizing changes the number of pixels, not just how the image looks on screen.

### 🔸 Crop
Cropping is just array slicing:

```python
cropped = img[y1:y2, x1:x2]
````

Use this to zoom into a region or extract a part of an image.

---
## 🔄 2. Rotate and Flip
### 🔁 Rotate
OpenCV uses rotation matrices. For simple 90°/180° turns, use:

```python
rotated = cv2.rotate(img, cv2.ROTATE_90_CLOCKWISE)
```

### ↔️ Flip
Flip horizontally (mirror) or vertically:

```python
flipped = cv2.flip(img, 1)  # Horizontal
```

---
## 🌗 3. Convert to Grayscale
Many tasks like edge detection or thresholding work better in grayscale.

```python
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
```

Now each pixel has one intensity value instead of 3.

---
## 🖊️ 4. Draw Shapes and Text
Useful for annotations, debugging, or creating synthetic data.

```python
cv2.rectangle(img, (x1, y1), (x2, y2), (255, 0, 0), thickness=2)
cv2.circle(img, center, radius, color, thickness)
cv2.putText(img, 'Label', (x, y), font, size, color, thickness)
```

---
## 🌀 5. Apply Filters (e.g., Blur)
Blur is often used to reduce noise or create artistic effects.

```python
blurred = cv2.GaussianBlur(img, (5, 5), 0)
```

Other filters:
-  cv2.medianBlur()
-  cv2.bilateralFilter()

These will be useful when we start preprocessing data for ML.

---
## 🚀 6. Hands-On Practice
👉 [Click here to open the notebook on Google Colab](https://github.com/rahmatheroza/vision-journal/blob/main/notebooks/03-image-processing-with-opencv.ipynb)
