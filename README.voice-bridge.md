# VoiceBridge - Multilingual Audio-to-Audio Translation Platform

VoiceBridge is a comprehensive real-time speech translation platform designed to bridge language gaps during live audio conversations. It performs speech recognition, translation, and text-to-speech synthesis to enable seamless multilingual communication, with specialized support for Indian languages.

## 🎯 Project Objectives

This project aims to create a complete audio-to-audio translation pipeline that:

- **Breaks down language barriers** in real-time conversations
- **Supports Indian languages** with high-quality synthesis using Facebook's MMS-TTS models
- **Provides modular architecture** for easy customization and deployment
- **Enables seamless integration** through RESTful APIs
- **Supports both monolithic and microservices deployment** patterns

## 🏗️ System Architecture

### Core Components

1. **Speech Recognition (ASR)**: OpenAI Whisper model for accurate transcription
2. **Translation Engine**: Google Translate API for multilingual support
3. **Text-to-Speech (TTS)**: Facebook MMS-TTS models optimized for Indian languages
4. **Romanization Support**: Uroman integration for non-Roman script handling

### Deployment Options

- **Monolithic Service** (`main.py`): All-in-one endpoint for complete audio-to-audio pipeline
- **Microservices Architecture**: 
  - Whisper Server (`whisper_server.py`): Dedicated ASR service
  - TTS Server (`tts_server.py`): Dedicated text-to-speech service

## 🚀 Key Features

### 🎙️ Advanced Speech Recognition
- **OpenAI Whisper Medium Model** for high-accuracy transcription
- **Multi-format audio support** (WAV, MP3, etc.)
- **Robust noise handling** and audio preprocessing

### 🌍 Comprehensive Translation Support
- **Google Translate integration** for 100+ languages
- **Async/sync translation handling** with fallback mechanisms
- **Optional translation step** for monolingual use cases

### 🔊 High-Quality Speech Synthesis
- **Facebook MMS-TTS models** optimized for Indian languages
- **Support for 20+ Indian languages** including:
  - Hindi (हिन्दी)
  - Bengali (বাংলা)
  - Tamil (தமிழ்)
  - Telugu (తెలుగు)
  - Kannada (ಕನ್ನಡ)
  - Malayalam (മലയാളം)
  - Marathi (मराठी)
  - Gujarati (ગુજરાતી)
  - Punjabi (ਪੰਜਾਬੀ)
  - Odia (ଓଡ଼ିଆ)
  - Assamese (অসমীয়া)
  - Urdu (اردو)
  - And more...

### 🛠️ Technical Excellence
- **Uroman romanization** for non-Roman scripts
- **GPU acceleration support** (CUDA-enabled)
- **Model caching** with LRU cache for optimal performance
- **Error handling and fallback mechanisms**
- **Deterministic synthesis** with seed control

### 🐳 Production-Ready Deployment
- **Multiple Dockerfiles** for different deployment scenarios
- **Containerized services** for scalability
- **RESTful API design** for easy integration
- **Health checks and monitoring** capabilities

## 📋 Supported Languages

The platform supports comprehensive Indian language coverage:

| Language | Google Code | MMS Model | Script Support |
|----------|-------------|-----------|----------------|
| Hindi | hi | facebook/mms-tts-hin | Devanagari |
| Bengali | bn | facebook/mms-tts-ben | Bengali |
| Tamil | ta | facebook/mms-tts-tam | Tamil |
| Telugu | te | facebook/mms-tts-tel | Telugu |
| Kannada | kn | facebook/mms-tts-kan | Kannada |
| Malayalam | ml | facebook/mms-tts-mal | Malayalam |
| Marathi | mr | facebook/mms-tts-mar | Devanagari |
| Gujarati | gu | facebook/mms-tts-guj | Gujarati |
| Punjabi | pa | facebook/mms-tts-pan | Gurmukhi |
| Odia | or | facebook/mms-tts-ori | Odia |
| Assamese | as | facebook/mms-tts-asm | Bengali |
| Urdu | ur | facebook/mms-tts-urd | Arabic |
| Nepali | ne | facebook/mms-tts-nep | Devanagari |
| Sanskrit | sa | facebook/mms-tts-san | Devanagari |
| And more... | | | |

## � Use Cases

### Primary Applications
- **Live conference translation** for multilingual meetings
- **Educational content localization** 
- **Customer service automation** in multiple Indian languages
- **Accessibility tools** for hearing-impaired users
- **Cross-cultural communication** platforms
- **Voice-based chatbots** with multilingual support

### Integration Scenarios
- **Mobile applications** for real-time translation
- **Web platforms** for voice-enabled services
- **IoT devices** with voice interfaces
- **Call center solutions** for multilingual support
- **E-learning platforms** for language learning

## 🏃‍♂️ Quick Start

### Monolithic Deployment
```bash
# Build and run the main service
docker build -f Dockerfile.main -t voice-bridge-main .
docker run -p 8000:8000 voice-bridge-main
```

### Microservices Deployment
```bash
# TTS Service
docker build -f Dockerfile.tts -t voice-bridge-tts .
docker run -p 8001:8000 voice-bridge-tts

# Whisper Service  
docker build -f Dockerfile.whisper -t voice-bridge-whisper .
docker run -p 8002:8000 voice-bridge-whisper
```

## � API Endpoints

### Main Service (`/audio-to-audio`)
Complete audio-to-audio translation pipeline:
- **Input**: Audio file + language parameters
- **Output**: Translated audio file
- **Features**: Speech recognition, translation, and synthesis

### Microservices
- **Whisper Service** (`/transcribe`): Audio-to-text conversion
- **TTS Service** (`/tts`): Text-to-speech synthesis

## 🎯 Technical Innovation

### Advanced Features
- **Synchronous and asynchronous processing** support
- **Memory-efficient model loading** with caching
- **Multi-GPU support** for scaled deployments  
- **Script-aware romanization** using Uroman
- **Robust error handling** with detailed logging
- **Configurable quality settings** for different use cases

### Performance Optimizations
- **Model pre-loading** during container startup
- **LRU caching** for frequently used models
- **GPU acceleration** when available
- **Efficient audio processing** with scipy and numpy
- **Memory management** for large audio files