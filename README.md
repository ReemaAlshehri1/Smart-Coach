# Smart-Coach
This project aims to support football coaches in making better decisions by automatically analyzing players’ emotions and physical movements from match videos.  It uses AI models to detect facial emotions and track each player’s speed, direction, and position over time. Then, it combines both  data to generate  psychological  insights by LLM.
### 🔍 Built With:
- Python
- OpenCV
- PyTorch
- HuggingFace Transformers
- MTCNN / DeepSort
- ResNet18
- Google Colab

### 🏆 Built During:
AI League Hackathon by Sky & Tuwaiq Academy

### 📂 Files:
- model.py:train  a custom emotion classification model (based on pretrained resnet18) on a manually collected dataset of football plyers' facial expressions.
- report_generator.py: Generates player psychological insight using local LLM.
- vedio_processing.py: Processes video and tracks players to classify their emotions and detect theit physical info, then generate a json report that contains these info.
- Faces_dataset.zip: a Custom labeld dataset containing facial images of football plyers and corresponding emotion labels used for training.
