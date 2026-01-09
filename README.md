Speech-to-Text using Whisper ASR
This project showcases the capabilities of the Whisper automatic speech recognition (ASR) system by OpenAI. Whisper is a state-of-the-art ASR model trained on a diverse range of speech data. It is capable of transcribing audio files and performing language detection and translation.

Getting Started
Prerequisites
Before running this project, make sure you have the following libraries and dependencies installed:

Python 3.x
PyTorch
Whisper
PyTube
Librosa
IBM Watson (for language detection)
Install the required libraries using the provided instructions.

Installing Required Libraries
# Install required libraries
!pip install torch
!pip install --upgrade torch
!pip install pytube
!pip install git+https://github.com/openai/whisper.git
!pip install git+https://github.com/librosa/librosa
Please restart the kernel after running the above installs.

Usage
This project demonstrates various functionalities of Whisper ASR, including:

Loading and processing audio files.
Language detection using Whisper.
Transcription of audio files.
Translation of transcribed text.
Loading the Models
There are five model sizes, four with English-only versions, offering speed and accuracy trade-offs. Below are the names of the available models and their approximate memory requirements and relative speed. You can use the tiny model for light weight applications, the large model if accuracy is most important, and the base or medium models for everything in between.



Table Source: openai/whisper

Whisper offers different model sizes optimized for speed and accuracy. The medium model is used in this project.

Loading the File
You can load your own audio file by replacing the file_path variable with the path to your audio file.

Language Detection
The sample audio is automatically detected for its spoken language. The detection is performed using the Whisper ASR system.

Decoding and Transcription
The whisper.decode() function processes 30 seconds of audio segment, while the transcribe() method reads the entire file, performing autoregressive sequence-to-sequence predictions on each window.

Translation
You can translate the audio file to different languages by setting the language parameter in the transcribe() method.

Transcription from YouTube
This project also supports transcribing audio from YouTube videos. Simply provide the URL of the video, and the audio will be processed and transcribed.
