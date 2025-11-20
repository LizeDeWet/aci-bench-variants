# ACI-Bench Dataset and ASR-Degraded Variant

## Overview
This repository contains the original ACI-Bench dataset, along with an ASR-degraded variant created to simulate real-world automatic speech recognition (ASR) errors in clinical conversation transcripts.


## Data Description

### 1. Original ACI-Bench Dataset
The original dataset was introduced in:

**Aci-bench: A Novel Ambient Clinical Intelligence Dataset for Benchmarking Automatic Visit Note Generation**  
Wen-wai Yim, Yujuan Fu, Asma Ben Abacha, Neal Snider, Thomas Lin, Meliha Yetisgen.  
*Submitted to Nature Scientific Data (2023).*  
https://www.nature.com/articles/s41597-023-02487-3

The ACI-Bench dataset contains synthetic doctor–patient dialogues paired with corresponding note summaries of the primary care visit.

### 2. ASR-Degraded Variant (Created for Further Research)
To evaluate model resilience to imperfect ASR transcription, an ASR-degraded version of the dialogue transcripts was created.

**Process:**
1. **Text-to-Speech (TTS):** Microsoft Azure Text-to-Speech was used to convert the original ACI-Bench text dialogues into synthetic audio.
2. **Automatic Speech Recognition (ASR):** The generated audio was transcribed using OpenAI Whisper, introducing ASR-style errors.
3. **Data Structure:** Each ASR transcript corresponds to its original dialogue ID.

## Repository Structure

- data/
    - src_experiment_data/
        - {train,valid,clinicalnlptaskB_test1,clinicalnlp_taskC_test2,clef_taskC_test3}.csv
        - {train,valid,clinicalnlptaskB_test1,clinicalnlp_taskC_test2,clef_taskC_test3}_metadata.csv
    - challenge_data/
        - {train_aci,valid_aci,test1_aci,test2_aci,test3_aci}_{asrcorr,asr}.csv
        - {train_aci,valid_aci,test1_aci,test2_aci,test3_aci}_{asrcorr,asr}_metadata.csv
        - {train_virtscribe,valid_virtscribe,test1_virtscribe,test2_virtscribe,test3_virtscribe}_{humantrans,asr}.csv
        - {train_virtscribe,valid_virtscribe,test1_virtscribe,test2_virtscribe,test3_virtscribe}_{humantrans,asr}_metadata.csv
├── data/

  ├── original/ # Unmodified ACI-Bench dialogues + summaries

├── asr_degraded/ # Whisper-transcribed dialogues with ASR errors

├── audio/ # (Optional) Azure TTS audio files

└── README.md


## Citation
The original ACI-Bench dataset:

```
@article{aci-bench,
  author = {Wen{-}wai Yim and
                Yujuan Fu and
                Asma {Ben Abacha} and
                Neal Snider and Thomas Lin and Meliha Yetisgen},
  title = {ACI-BENCH: a Novel Ambient Clinical Intelligence Dataset for Benchmarking Automatic Visit Note Generation},
  journal = {Nature Scientific Data},
  year = {2023}
}
```

## Contact
Lize de Wet, GitHub: LizeDeWet
