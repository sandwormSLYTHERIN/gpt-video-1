# GPT with Vision for Video Understanding

## Overview

This project demonstrates how multimodal large language models can be used for **video understanding, scene narration, and automated voiceover generation** by combining frame extraction, visual reasoning, and text-to-speech synthesis.

Since current vision-language models do not directly process raw video streams end-to-end, the pipeline converts video into representative image frames and uses those frames as visual context for language generation.

The system performs:

* Video frame extraction
* Visual scene understanding using GPT vision models
* Narrative generation from temporal visual context
* Voiceover script generation
* Audio narration synthesis using text-to-speech APIs

---

## Pipeline Architecture

### 1. Frame Extraction

* Used **OpenCV** to load video input
* Extracted frames sequentially from video stream
* Encoded frames into **base64 JPEG format** for model-compatible transmission

### 2. Visual Reasoning

* Sent sampled frames to **GPT vision-capable multimodal model**
* Generated scene-level descriptions by interpreting temporal visual content across multiple frames

### 3. Narrative Generation

* Prompted the model to produce coherent descriptions suitable for:

  * video captions
  * content summaries
  * descriptive narration

### 4. Voiceover Synthesis

* Generated narration scripts from visual understanding output
* Converted generated text into speech using **GPT-4o TTS API**
* Controlled tone, pacing, and narration style through voice instructions

---

## Tech Stack

* Python
* OpenCV
* OpenAI API
* Base64 Encoding
* GPT Vision Models
* GPT-4o Text-to-Speech

---

## Key Features

* Converts raw video into interpretable multimodal input
* Produces natural language scene descriptions
* Generates style-controlled narration scripts
* Synthesizes audio output directly from generated text

---

## Example Use Cases

* Automated video caption generation
* Surveillance scene summarization
* Educational narration pipelines
* Accessibility tools for video content
* Voice-assisted media annotation

---

## Implementation Notes

* Frames are sampled instead of sending the full video to reduce token usage
* Temporal understanding depends heavily on frame selection strategy
* Different prompting styles significantly affect narration quality

---

## Future Improvements

* Adaptive frame sampling based on motion intensity
* Multi-scene segmentation before prompting
* Timestamp-aware narration generation
* Integration with local speech synthesis for offline deployment

---

## Note

Due to technical limitations in the current uploading environment, only a **sample subset of the full workflow has been executed and uploaded for demonstration purposes**.
