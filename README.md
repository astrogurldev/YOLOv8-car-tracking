# 🚗 YOLOv8 Car Detection & Tracking

A computer vision pipeline that detects and tracks cars in video using Ultralytics YOLOv8 and OpenCV. Built as part of a Computer Vision internship test.

## 📽️ Demo
[▶️ Watch the output video here](https://drive.google.com/file/d/1WMmYnzJyDh5CCq4iciUDrXVw5leoKR2y/view?usp=sharing)

## 🛠️ Tech Stack
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics) — object detection & tracking
- OpenCV — video I/O and annotation
- FFmpeg — video conversion to H.264/MP4
- Google Colab — development environment

## ⚙️ How It Works
1. Load YOLOv8 pretrained model (`yolov8n.pt`) trained on COCO dataset
2. Read input video frame by frame using OpenCV
3. Run `model.track(persist=True)` for detection + persistent tracking IDs
4. Filter results to **car only** (COCO class ID `2`) with confidence ≥ 50%
5. Draw bounding boxes and track IDs on each frame
6. Export annotated video, convert to H.264/MP4 via FFmpeg

## 📁 Project Structure
YOLOv8-car-tracking/
├── YOLO.ipynb        # Main notebook (detection + tracking pipeline)
├── README.md

## 🚀 Run it Yourself
1. Open `YOLO.ipynb` in Google Colab
2. Enable GPU: Runtime → Change runtime type → T4 GPU
3. Upload your video file
4. Update `INPUT_VIDEO` variable with your filename
5. Run all cells

## 📦 Requirements
