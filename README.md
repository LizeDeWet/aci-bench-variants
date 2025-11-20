# ACI-Bench Dataset and ASR-Degraded Variant

## Overview
This repository contains the original ACI-Bench dataset, along with an ASR-degraded variant created to simulate real-world automatic speech recognition (ASR) errors in clinical conversation transcripts.

---

## Data Description

### 1. Original ACI-Bench Dataset
The original dataset was introduced in:

**Aci-bench: A Novel Ambient Clinical Intelligence Dataset for Benchmarking Automatic Visit Note Generation**  
Wen-wai Yim, Yujuan Fu, Asma Ben Abacha, Neal Snider, Thomas Lin, Meliha Yetisgen.  
*Submitted to Nature Scientific Data (2023).*  
https://www.nature.com/articles/s41597-023-02487-3

The ACI-Bench dataset contains synthetic doctor–patient dialogues paired with corresponding note summaries of the primary care visit.
The original dataset files are located in:

/original/

---

### 2. ASR-Degraded Variant (Created for Further Research)
To evaluate model resilience to imperfect ASR transcription, an ASR-degraded version of the dialogue transcripts was created.

**Process:**
1. **Text-to-Speech (TTS):** Microsoft Azure Text-to-Speech was used to convert the original ACI-Bench text dialogues into synthetic audio.
2. **Automatic Speech Recognition (ASR):** The generated audio was transcribed using OpenAI Whisper, introducing ASR-style errors.
3. **Data Structure:** Each ASR transcript corresponds to its original dialogue ID.

The ASR transcripts are located in:

/asr_degraded/

---

## Repository Structure

.
├── README.md
├── original/ # Unmodified ACI-Bench dialogues + summaries
├── asr_degraded/ # Whisper-transcribed dialogues with ASR errors
├── audio/ # (Optional) Azure TTS audio files
└── metadata/ # (Optional) Supporting files or mappings

---

## Citation
The original ACI-Bench dataset:

Aci-bench: a Novel Ambient Clinical Intelligence Dataset for Benchmarking Automatic Visit Note Generation". Wen-wai Yim, Yujuan Fu, Asma Ben Abacha, Neal Snider, Thomas Lin, Meliha Yetisgen. Submitted to Nature Scientific Data, 2023. https://www.nature.com/articles/s41597-023-02487-3

Contact
Lize de Wet
GitHub: LizeDeWet
