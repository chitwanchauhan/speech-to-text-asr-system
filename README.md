
#  **README.md**

```markdown
# 🎙️ Hindi ASR Pipeline using Whisper-small

An end-to-end Automatic Speech Recognition (ASR) project for Hindi speech data using Whisper-small.  
This project covers data preprocessing, baseline evaluation, fine-tuning, error analysis, and transcript cleanup.

---

##  Project Overview

This project focuses on building and analyzing a Hindi ASR system using Whisper-small.  
It includes:

- Dataset preprocessing from raw audio + transcription URLs  
- Baseline evaluation using pretrained Whisper-small  
- Model fine-tuning (experimental)  
- Word Error Rate (WER) evaluation  
- Transcript cleanup pipeline (number normalization + English word detection)  
- Spelling error analysis for dataset improvement  

---

##  Project Structure

```

ASR-Hindi-Speech-Recognition-Pipeline/
│
├── 01_data_preparation.ipynb        # Data loading & preprocessing
├── 02_baseline_fleurs_eval.ipynb   # Baseline evaluation on FLEURS dataset
├── 03_whisper_finetune.ipynb       # Fine-tuning Whisper-small
├── 04_final_evaluation.ipynb       # Evaluation & WER calculation
├── 05_cleanup_pipeline.ipynb       # Text post-processing pipeline
├── 06_spelling_analysis.ipynb      # Word-level spelling analysis
│
└── README.md

```

---

##  Technologies Used

- Python  
- Whisper (OpenAI)  
- NumPy / Pandas  
- Google Colab  

---

##  Key Components

### 1. Data Preprocessing
- Extracted audio and transcription from cloud URLs  
- Cleaned and structured Hindi dataset  
- Prepared inputs for ASR pipeline  

---

### 2. Baseline ASR Evaluation
- Used pretrained Whisper-small model  
- Generated raw transcripts  
- Compared predictions with ground truth  

---

### 3. Word Error Rate (WER)
- Evaluated model performance using WER  
- Compared predictions vs reference transcripts  

---

### 4. Transcript Cleanup Pipeline

####  Number Normalization
- Converted Hindi number words → digits  
- Example:
```

दो → 2
तीन सौ → 300

```

####  English Word Detection
- Identified English-origin words in Hindi transcripts  
- Tagged using:
```

[EN]word[/EN]

```

---

### 5. Error Analysis
- Sampled incorrect predictions  
- Identified common error types:
- Phonetic errors  
- Word omission  
- Spelling variations  

---

### 6. Spelling Analysis
- Analyzed ~1.7L unique words  
- Classified words as:
- Correct  
- Incorrect  
- Assigned confidence levels (high / medium / low)  

---

##  Sample Output

```

Ground Truth: मेरा नाम chitwan है
Prediction: मेरा नाम chitvan

```

---

##  Limitations

- Fine-tuning was limited due to compute constraints  
- Rule-based cleanup pipeline may fail in edge cases  
- Spelling classification struggles with rare words and names  

---

##  Future Improvements

- Use larger datasets for better fine-tuning  
- Implement context-aware normalization  
- Improve English word detection using NLP models  
- Apply lattice-based evaluation for flexible scoring  

---

##  Author

**Chitwan Chauhan**  
B.Tech CSE (AI/ML)  
Focused on AI, ML, and real-world problem solving  

---

##  Note

This project was developed as part of an ASR research assignment to explore real-world speech processing challenges in Hindi.

---
```

---

