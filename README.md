# Implementation of FastSpeech 2-Based Text-to-Speech Synthesis

Assignment: English (Svarah) & Telugu (IndicTTS Telugu) | Deadline: 07-11-2026

Based on ming024/FastSpeech2: https://github.com/ming024/FastSpeech2

## Folder Structure (Exact as Required)
project/
├── English/
│   ├── train.py
│   ├── preprocess.py
│   ├── inference.py
│   ├── config.yaml
│   └── checkpoints/
├── Telugu/
│   ├── train.py
│   ├── preprocess.py
│   ├── inference.py
│   ├── config.yaml
│   └── checkpoints/
├── Results/
│   ├── English/
│   │   ├── training_loss.png
│   │   ├── validation_loss.png
│   │   ├── test_generated_audios/
│   │   └── variance_adaptor_plots/duration/ pitch/ energy/
│   └── Telugu/ (same)
├── Report/
│   └── Technical_Report.pdf
├── README.md
└── requirements.txt

## Datasets
- English: Svarah - 5h train, 1h val, no overlap
- Telugu: IndicTTS Telugu - same split, seed 42

## Telugu Changes
- Unicode NFC normalization U+0C00-U+0C7F
- Deeper decoder (6 layers)
- Transliteration for mixed words like 'andaroo'

## Run
pip install -r requirements.txt
cd project/English
python preprocess.py
python train.py
python inference.py
cd ../Telugu
python preprocess.py
python train.py
python inference.py

## GitHub Deploy - See DEPLOY_GUIDE.md
