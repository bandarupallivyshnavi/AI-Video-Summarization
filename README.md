# AI Video Summarization

An interactive frontend prototype for an AI-powered video summarization system. The project demonstrates how a long video can be transformed into a concise summary with important moments, timestamps, and topic labels.

> **Portfolio prototype:** the current demo simulates the ML inference stage in the browser. The architecture is designed to connect to a real Python/FastAPI model backend.

## Problem

Long videos are time-consuming to watch when a user only needs the most important information. The goal is to automatically identify relevant content and present it as a short, structured summary.

## Solution

**Video Upload → Preprocessing → Frame/Feature Extraction → Temporal Analysis → Key Moment Selection → Summary Generation → User Interface**

The prototype presents:
- Concise generated summary
- Key moments with timestamps
- Topic tags
- Original vs. summary duration
- Compression percentage

## ML Pipeline

A production implementation can combine video decoding/frame sampling, CNN or Transformer-based visual feature extraction, temporal modeling, importance scoring, and natural-language generation.

## Architecture

See `architecture.svg` for the system design.

## Run Locally

Open `index.html` in a browser. No installation is required for the current prototype.

## Production API Design

```text
POST /api/summarize
Content-Type: multipart/form-data

video: <uploaded video>

Response:
{
  "summary": "...",
  "duration": 754,
  "summary_duration": 138,
  "compression": 81.7,
  "key_moments": [
    {"timestamp": "00:42", "title": "Introduction"},
    {"timestamp": "03:15", "title": "Main Concept"}
  ]
}
```

## Future Improvements

- Real-time frame extraction
- Audio transcription with Whisper
- Multimodal visual + audio summarization
- Transformer-based temporal modeling
- User-selectable summary length
- Downloadable summaries
- FastAPI deployment and Dockerization
- ROUGE and temporal coverage evaluation

## Skills

Python • Machine Learning • Deep Learning • Computer Vision • Video Processing • Data Preprocessing • Model Evaluation • API Integration • Problem Solving

## License

This project is intended as a portfolio/academic prototype.
