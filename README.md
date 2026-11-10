# OpenCV Crash Course: 2026 Edition

Short, modern OpenCV course. No camera or Raspberry Pi needed.

## Setup

```bash
venv\Scripts\activate
pip install opencv-contrib-python matplotlib numpy ultralytics "supervision[assets]" onnx onnxruntime
pip install easyocr
pip uninstall -y opencv-python-headless
```

The last line matters: EasyOCR installs a second "headless" OpenCV that breaks `cv2.imshow` (webcam window).

## Modules (one notebook = one video)

| # | Notebook | Topic | Time |
|---|---|---|---|
| 1 | `01_intro_basics` | Read/save, color spaces, resize, crop, rotate | 30 min |
| 2 | `02_image_processing` | Blur, threshold, Canny, morphology, CLAHE | 30 min |
| 3 | `03_contours_drawing` | Drawing, contours, bounding boxes | 20 min |
| 4 | `04_video_realtime` | Video loop, FPS, webcam/RTSP | 20 min |
| 5 | `05_yolo_detection` | YOLO26 detection | 15 min |
| 6 | `06_tracking_counting` | Tracking + line counter | 15 min |
| 7 | `07_custom_training` | Train on your own data | 20 min |
| 8 | `08_segmentation` | YOLO-seg + SAM | 15 min |
| 9 | `09_ocr` | Read text and numbers | 15 min |
| 10 | `10_onnx_deployment` | ONNX export + speed | 15 min |

## Folders (created automatically when you run the notebooks)

| Folder | What's inside |
|---|---|
| `input/` | Images and videos we read |
| `output/` | Images and videos we save |
| `models/` | Model files (`.pt`, `.onnx`) |
| `scripts/` | Webcam `.py` scripts made by modules 4 and 5 |
| `runs/` | Training results from module 7 |
| `datasets/` | Training dataset from module 7 |
