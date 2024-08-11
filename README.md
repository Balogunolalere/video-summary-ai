# Video Summary AI

Video Summary AI is an advanced video summarization system that automatically extracts key frames from a video, generates descriptions for these frames, and creates a concise summary video with text descriptions. This tool is perfect for quickly understanding the content of long videos or creating highlights from video footage.

## Features

- Automatic scene detection
- Key frame extraction using computer vision techniques
- Image captioning with state-of-the-art AI models
- Intelligent frame selection using clustering algorithms
- Generation of text summaries for the entire video
- Creation of a summary video with key frames

## Prerequisites

- Python 3.7+
- OpenCV
- PyTorch
- torchvision
- Transformers
- scikit-learn
- matplotlib
- moviepy
- Other dependencies (see `requirements.txt`)

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/Balogunolalere/video-summary-ai.git
   cd video-summary-ai
   ```

2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Usage

1. Place your input video in the project directory or specify the path to your video.

2. Run the main script:
   ```
   python video_summarization_system.py
   ```

3. The script will process the video and generate:
   - A text summary of the video
   - Visualizations of key frames
   - A summary video

4. The summary video will be saved as `summary_video.mp4` in the project directory.

## How It Works

1. **Scene Detection**: The video is analyzed to detect scene changes using PySceneDetect.
2. **Frame Extraction**: Key frames are extracted from each detected scene.
3. **Feature Extraction**: A ResNet50 model is used to extract features from each key frame.
4. **Image Captioning**: Each key frame is captioned using the BLIP image captioning model.
5. **Frame Selection**: K-means clustering is applied to select the most representative frames.
6. **Summary Generation**: A text summary is generated based on the captions of the selected frames.
7. **Video Creation**: A summary video is created using the selected frames and their captions.

## Customization

- Adjust the `num_keyframes` parameter in the `summarize_video` function to change the number of frames in the summary.
- Modify the `duration_per_frame` parameter in the `create_summary_video` function to change the duration of each frame in the summary video.
- Experiment with different image captioning models by changing the model in the `pipeline` function.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

- [PySceneDetect](https://github.com/Breakthrough/PySceneDetect) for scene detection
- [Hugging Face Transformers](https://github.com/huggingface/transformers) for the image captioning model
- [scikit-learn](https://scikit-learn.org/) for K-means clustering
- [moviepy](https://zulko.github.io/moviepy/) for video editing capabilities