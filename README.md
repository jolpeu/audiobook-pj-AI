# Emotion Sound Effect API

This project provides an API for emotion recognition from text (e.g., OCR from PDF) and recommends appropriate sound effects based on the predicted emotion.

## Features

- Upload a storybook PDF
- Automatically extract sentences
- Predict emotion using a fine-tuned RoBERTa model
- Recommend a sound effect per sentence

## Local Setup

```bash
# Install dependencies
pip install -r requirements.txt

# Run the FastAPI app
python -m uvicorn main:app --reload
```

## API Endpoints

### `POST /predict_pdf`
Upload a PDF and receive a list of sentences with predicted emotion and matching sound effect.

```json
[
  {
    "sentence": "The boy was crying in the corner.",
    "emotion": "슬픔",
    "effect_file": "rain.wav"
  },
  ...
]
```

## Folder Structure

```
finetuned_emotion_model/      # Huggingface model
ESC-50-master/audio/          # ESC-50 audio files
```

Make sure these folders exist with the correct files before running the server.
