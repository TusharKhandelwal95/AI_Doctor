# AI Doctor 
**Medical Chatbot with Multimodal LLM (Vision and Voice)**  

## Project Overview  
AI Doctor is an advanced medical chatbot designed to assist users by leveraging multimodal Large Language Models (LLMs) for vision and voice capabilities. It processes medical images, transcribes patient audio, and responds with natural-sounding speech through an intuitive user interface.  

## Features  
- **Medical Image Analysis**: Uses Llama 3 Vision to process and interpret medical images.  
- **Speech-to-Text**: Records patient speech and transcribes it using OpenAI Whisper.  
- **Text-to-Speech**: Converts doctor responses into natural-sounding voice with gTTS and ElevenLabs.  
- **Interactive UI**: A Gradio-based interface for seamless interaction.  

## Project Layout  
1. **Phase 1**: Set up the Multimodal LLM for image processing.  
   - Configure Groq API key.  
   - Convert images into the required format.  

2. **Phase 2**: Implement patient audio input.  
   - Set up audio recording with `ffmpeg` and `portaudio`.  
   - Transcribe audio using Speech-to-Text models (STT).  

3. **Phase 3**: Enable doctor voice output.  
   - Integrate Text-to-Speech models (TTS) with gTTS and ElevenLabs.  

4. **Phase 4**: Develop the user interface.  
   - Create an interactive Gradio-based VoiceBot UI.  

## Tools and Technologies  
- **LLMs**: Llama 3 Vision (Meta)  
- **Audio Processing**: OpenAI Whisper, gTTS, and ElevenLabs  
- **User Interface**: Gradio  
- **Development**: Python and VS Code  

## Technical Architecture  
1. **Multimodal Inference**: Groq API for optimized LLM inference.  
2. **Speech Processing**: Whisper for transcription; TTS for voice response.  
3. **User Experience**: Gradio for interactive communication.  

## Future Enhancements  
- Use advanced state-of-the-art LLMs, including paid vision models.  
- Fine-tune the vision model on specialized medical imaging datasets.  
- Incorporate multilingual capabilities for greater accessibility.  


# Project Setup Guide

This guide provides step-by-step instructions to set up your project environment, including the installation of FFmpeg and PortAudio across macOS, Linux, and Windows, as well as setting up a Python virtual environment using Pipenv, pip, or conda.

## Table of Contents

1. [Installing FFmpeg and PortAudio](#installing-ffmpeg-and-portaudio)
   - [macOS](#macos)
   - [Linux](#linux)
   - [Windows](#windows)
2. [Setting Up a Python Virtual Environment](#setting-up-a-python-virtual-environment)
   - [Using Pipenv](#using-pipenv)
   - [Using pip and venv](#using-pip-and-venv)
   - [Using Conda](#using-conda)
3. [Running the application](#project-phases-and-python-commands)

## Installing FFmpeg and PortAudio

### macOS

1. **Install Homebrew** (if not already installed):

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Install FFmpeg and PortAudio:**

   ```bash
   brew install ffmpeg portaudio
   ```


### Linux
For Debian-based distributions (e.g., Ubuntu):

1. **Update the package list**

```
sudo apt update
```

2. **Install FFmpeg and PortAudio:**
```
sudo apt install ffmpeg portaudio19-dev
```

### Windows

#### Download FFmpeg:
1. Visit the official FFmpeg download page: [FFmpeg Downloads](https://ffmpeg.org/download.html)
2. Navigate to the Windows builds section and download the latest static build.

#### Extract and Set Up FFmpeg:
1. Extract the downloaded ZIP file to a folder (e.g., `C:\ffmpeg`).
2. Add the `bin` directory to your system's PATH:
   - Search for "Environment Variables" in the Start menu.
   - Click on "Edit the system environment variables."
   - In the System Properties window, click on "Environment Variables."
   - Under "System variables," select the "Path" variable and click "Edit."
   - Click "New" and add the path to the `bin` directory (e.g., `C:\ffmpeg\bin`).
   - Click "OK" to apply the changes.

#### Install PortAudio:
1. **Install Pyaudio (portaudio is already installed as a dependency package on windows.):**  
```
pip install pyaudio
```

---

## Setting Up a Python Virtual Environment

### Using Pipenv
1. **Install Pipenv (if not already installed):**  
```
pip install pipenv
```

2. **Install Dependencies with Pipenv:** 

```
pipenv install
```

3. **Activate the Virtual Environment:** 

```
pipenv shell
```

---

### Using `pip` and `venv`
#### Create a Virtual Environment:
```
python -m venv venv
```

#### Activate the Virtual Environment:
**macOS/Linux:**
```
source venv/bin/activate
```

**Windows:**
```
venv\Scripts\activate
```

#### Install Dependencies:
```
pip install -r requirements.txt
```

---

### Using Conda
#### Create a Conda Environment:
```
conda create --name myenv python=3.11
```

#### Activate the Conda Environment:
```
conda activate myenv
```

#### Install Dependencies:
```
pip install -r requirements.txt
```


# Project Phases and Python Commands

## Phase 1: Brain of the doctor
```
python brain_of_the_doctor.py
```

## Phase 2: Voice of the patient
```
python voice_of_the_patient.py
```

## Phase 3: Voice of the doctor
```
python voice_of_the_doctor.py
```

## Phase 4: Setup Gradio UI
```
python gradio_app.py
```

