# Whisper Hindi Model

The Whisper Hindi ASR (Automatic Speech Recognition) model utilizes the KathBath dataset, a comprehensive collection of speech samples in Hindi. Trained on this dataset, Whisper employs advanced deep learning techniques to accurately transcribe spoken Hindi into text. Its architecture harnesses the power of neural networks to recognize and interpret the nuances of the Hindi language, including regional accents and dialects. Whisper stands out for its efficiency and accuracy, offering a reliable solution for converting spoken Hindi into written text across various applications, from transcription services to voice-enabled interfaces.

The KathBath dataset serves as a crucial foundation for training the Whisper model. This dataset encompasses diverse speech samples sourced from different regions, covering a wide range of topics and conversational styles. The richness and diversity of the data enable Whisper to generalize well across various real-world scenarios, ensuring robust performance in different contexts.

ASR models not only transcribe speech but also calculate the Word Error Rate (WER) by comparing their output to a reference transcription. This metric quantifies accuracy, with lower WER values indicating better performance.

## Overview

This project aims to develop an effective and efficient ASR model for the Hindi language using state-of-the-art techniques. The model leverages the powerful Whisper framework, with additional data and evaluation metrics from Vistaar and ASR Evaluation tools. The primary focus is on enhancing the accuracy and robustness of speech recognition in Hindi.

## Datasets

The datasets used in this project are sourced from various platforms:

1. **Whisper**: [Whisper Dataset Link](https://github.com/openai/whisper)
2. **Vistaar**: [Vistaar Dataset Link](https://github.com/AI4Bharat/vistaar)
3. **ASR Evaluation**: [ASR Evaluation Dataset Link](https://github.com/belambert/asr-evaluation)
4. **Test Dataset**: [Test Dataset Link](https://asr.iitm.ac.in/Gramvaani/NEW/GV_Eval_3h.tar.gz)

Each dataset is carefully preprocessed and annotated to ensure high-quality training and evaluation.

## Model Architecture

The model architecture follows the standard pipeline of Whisper with modifications tailored for the Hindi language. Key components include:

- **Data Preprocessing**: Noise reduction, normalization, and augmentation techniques.
- **Feature Extraction**: Mel-frequency cepstral coefficients (MFCCs) and other relevant features.
- **Neural Network**: A deep learning model designed with layers optimized for ASR tasks.
- **Post-Processing**: Error correction and language modeling for better transcription accuracy.

![model_architecture_image](https://github.com/INurtureStudent/Whisper-Hindi-ASR-model/assets/120656373/53cc2725-0c4b-45ed-98ca-1bb5fd60001f)

## World Error Rate (WER):

Word Error Rate (WER) is a metric used to evaluate the performance of automatic speech recognition (ASR) systems. It measures the disparity between the transcribed output generated by the ASR system and the reference or ground truth transcription.
WER is calculated as the ratio of the total number of errors (insertions, deletions, and substitutions) required to align the transcribed text with the reference text, divided by the total number of words in the reference text.
WER provides a comprehensive assessment of the accuracy of ASR systems, taking into account both misrecognitions and omissions of words in the transcription. Lower WER values indicate higher accuracy, with a perfect score of 0 indicating an exact match between the transcribed and reference texts.
WER is a widely used evaluation metric in the field of speech recognition, providing valuable insights into the performance and quality of ASR models across different languages and applications.

# Setup

[](https://github.com/yashshekh/Whisper-Hindi-ASR-model#setup)

I have used Python 3.9.9 and PyTorch 1.10.1 to train and test our models, but the codebase is expected to be compatible with Python 3.8-3.11 and recent PyTorch versions. The codebase also depends on a few Python packages, most notably OpenAI's tiktoken for their fast tokenizer implementation. You can download and install (or update to) the latest release of Whisper with the following command:

```
  pip install -U openai-whisper

```

Alternatively, the following command will pull and install the latest commit from this repository, along with its Python dependencies:

```
  pip install git+https://github.com/openai/whisper.git

```

To update the package to the latest version of this repository, please run:

```
  pip install --upgrade --no-deps --force-reinstall git+https://github.com/openai/whisper.git

```

It also requires the command-line tool ffmpeg to be installed on your system, which is available from most package managers:

```
  #on Ubuntu or Debian
  sudo apt update && sudo apt install ffmpeg

  # on Arch Linux
  sudo pacman -S ffmpeg

  # on MacOS using Homebrew (https://brew.sh/)
  brew install ffmpeg

  # on Windows using Chocolatey (https://chocolatey.org/)
  choco install ffmpeg

  # on Windows using Scoop (https://scoop.sh/)
  scoop install ffmpeg
```
