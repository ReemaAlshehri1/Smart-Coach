# Smart-Coach
This project aims to support football coaches in making better decisions by automatically analyzing players’ emotions and physical movements from match videos.  It uses AI models to detect facial emotions and track each player’s speed, direction, and position over time. Then, it combines both  data to generate  psychological  insights by LLM.

###  Built With:
- Python
- OpenCV
- PyTorch
- HuggingFace Transformers
- MTCNN / DeepSort
- ResNet18
- Google Colab

###  Built During:
AI League Hackathon by Sky & Tuwaiq Academy


## Download the emotion Trained Model
You can download the trained model from [Google Drive](https://drive.google.com/file/d/1EBeqwMV4Vf_LlaFmW22PNjukdUYjOcXh/view?usp=sharing).

## How to run


1. Clone the repository:
   ```bash
   git clone https://github.com/ReemaAlshehri1/Smart-Coach.git
   cd Smart-Coach
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
3. Download the trained emotion recognition model:
   Ensure that emotion_model.pth is saved locally in your project folder.
4. Set your football match video URL:
In vedio_processing.py, replace the line that defines video_url with your match video link.
Example:
video_url = "https://your_match_video_link_here"
5. Set the model path in vedio_processing.py:
Update the line that loads the model with the path to your .pth file.
Example:
model.load_state_dict(torch.load('path_to/emotion_model.pth', map_location='cpu'))
6. Run the processing pipelin:
Run vedio_processing.py to process the video, detect faces, track players, and classify emotions.
7. Assign names to detected players:
The script will show player images. Enter a name when prompted for each Track ID.
A final report will be saved as Final_report_named.json.
8. Run the LLM feedback generation script:
Run llm_feedback.py to generate psychological evaluations for each player.
9. View output:
The script will print psychological evaluations for each player based on their emotional timeline and physical movement data.


###GitHub structure
Smart_Coach/
├── model.py                # Trains custom emotion classifier (ResNet18) on faces dataset
├── video_processing.py     # Processes match videos, tracks players, classifies emotions & extracts physical stats
├── llm_feedback.py         # Generates psychological feedback for each player using local LLM
├── Faces_dataset.zip       # Labeled facial images of football players and emotion labels
├── emotion_model.pth       # Trained emotion classification model
├── Final_report_named.json # Example JSON report from video processing
├── sample_video.mp4        # (Optional) short demo video clip
├── requirements.txt        # List of dependencies to install
└── README.md               # Project documentation


  
 ##  License
This project is not licensed for public use. All rights are reserved by the author.  
You may not copy, distribute, or modify this project without explicit permission.


