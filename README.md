# 🤖 OpenCV Live Video Detection Workshop

A hands-on, beginner-friendly Computer Vision workshop using **Python, OpenCV and YOLO**, built to run entirely in **Google Colab**. Most demos process a **live browser-camera feed** instead of a single captured photo.

## 📂 Repository Contents

| File | Description |
|---|---|
| `Week3_OpenCV_Live_Video_Detection_Workshop.ipynb` | Main workshop notebook |

## 🚀 Getting Started

1. Open the notebook in [Google Colab](https://colab.research.google.com/).
2. Run the install cell:
   ```python
   %pip -q install opencv-python-headless numpy matplotlib ultralytics
   ```
3. Run the cells in order, top to bottom.
4. Allow **camera permission** in your browser when prompted.
5. To stop a live demo, click **Runtime → Interrupt execution (■)**.

> Colab runs on a remote machine, so `cv2.VideoCapture(0)` cannot access your laptop camera. The notebook uses a browser-camera helper that streams frames into Python instead.

## 📚 What You'll Learn

- Basics of Computer Vision and how OpenCV works
- How images are stored as pixel arrays (grayscale and BGR)
- Core operations: load, grayscale, resize, crop, draw shapes and text
- Gaussian blur and Canny edge detection
- Colour detection using HSV
- Face detection with Haar Cascades
- Object detection with YOLO (`yolov8n.pt`)
- Testing a previously trained `.pkl` image classifier

## 🧪 Workshop Activities

| # | Activity | Concepts |
|---:|---|---|
| 1 | Load and display an image | Image reading |
| 2 | Convert to grayscale | `cvtColor` |
| 3 | Draw shapes and text | `rectangle`, `circle`, `putText` |
| 4 | Live edge detection | Canny |
| 5 | Live blue object tracking | HSV, contours |
| 6 | Live face detection | Haar Cascade |
| 7 | Live YOLO detection | Deep learning |

## 🎯 Projects

| Project | Description | Level |
|---|---|---|
| 4. Motion Detection | Frame differencing on live video | 🟡 Intermediate |
| 6. Invisible Cloak | Replace red cloth with a saved background | 🟡 Intermediate |
| 8. YOLO Object Counter | Count objects and people per frame | 🟡 Intermediate |
| 9. Eye Controlled Mouse | Reference / design activity | 🔴 Advanced |
| 10. Eye-Tracking Mouse Control | Reference / design activity | 🔴 Advanced |
| 11. Virtual Keyboard (Hand Gestures) | Reference / design activity | 🔴 Advanced |

> **Colab limitation:** Projects 9–11 need to control the local mouse/keyboard, which Colab cannot do. They are included as concept and design activities only.

## 🧩 Final Activity: Test Your Own `.pkl` Classifier

Upload your Week 2 trained model and a test image, then run a prediction. Make sure preprocessing matches training:

- [ ] Same image size
- [ ] Same colour conversion (grayscale or colour)
- [ ] Same channel order (RGB/BGR)
- [ ] Same normalization and flattening
- [ ] Same label mapping

> ⚠️ **Security:** only load `.pkl` files you created or trust. Pickle files can execute code when loaded.

## 📦 Requirements

| Library | Purpose |
|---|---|
| `opencv-python-headless` | Image processing in Colab |
| `numpy` | Arrays and masks |
| `matplotlib` | Inline image display |
| `ultralytics` | YOLO detection |

## 🛠️ Troubleshooting

| Problem | Fix |
|---|---|
| Camera permission denied | Allow camera access via the lock icon in the address bar, then rerun |
| Live feed is slow | Use `yolov8n.pt` or a GPU runtime |
| `ModuleNotFoundError` | Rerun the install cell, then restart the session |
| `cv2.imshow()` errors | Use Matplotlib for inline display |

## 📄 License

MIT License
