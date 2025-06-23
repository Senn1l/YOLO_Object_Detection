# YOLO Object Detection
This is a two-part project combining Flask-based object detection and YOLO model training.
## Project Structure
- `pretrained_inference/`: Flask app using pretrained YOLOv5 model for object detection.
- `custom_training/`: Flask app using a custom-trained YOLOv7 model, along with training notebook and inference results.
- `report/`: Project report in both PDF and DOCX formats.

## 1. Pretrained Inference
- Familiarized myself with Flask.
- Used the pretrained YOLOv5m model (Ultralytics) to detect objects.

## 2. Custom Training
- Trained a YOLOv7 model on a custom dataset using Google Colab and Google Drive.
- Used WongKinYiu's [YOLOv7 repository](https://github.com/WongKinYiu/yolov7?tab=readme-ov-file).
- The training pipeline is shown in `YOLOv7_train_custom.ipynb`.
- Final weights were exported and later loaded on the Flask app for inference.
- The trained model file (`last.pt`) is stored inside the Flask app folder.

## How to run the Flask app (with Miniconda)
- I used Miniconda (mini version of Anaconda) to run flask app.
1. Install [miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main).
3. Open miniconda (with Administrator) and install dependencies: flask, torch, opencv-python.
4. Navigate to the appropriate Flask app folder. Eg: cd <...>/pretrained_inference
5. Run the Flask app: python object_detection.py.
7. Visit http://127.0.0.1:5000 in your browser.
