# Modeling Human Activity States Using Hidden Markov Models

A Hidden Markov Model implemented from scratch in NumPy (Baum-Welch training and Viterbi decoding) that recognises four activities (standing, walking, jumping, still) from smartphone accelerometer and gyroscope data recorded with Sensor Logger.

**Author:** Carla Batoni, African Leadership University

## Repository contents

| Folder | Contents |
|---|---|
| `data/standing`, `data/walking`, `data/jumping`, `data/still` | 15 labelled training clips each (60 in total), 6-9 s each, with a timestamp column |
| `data/test` | 2 unseen test recordings (`test_01.csv`, `test_02.csv`), about 61 s each, containing all four activities |
| `notebook/hmm_activity_recognition.ipynb` | Full pipeline: cleaning, features, HMM, evaluation |
| `report/report.pdf` | Short report with results and discussion |

## Data
- Device: iPhone 13 Pro, Sensor Logger app; accelerometer and gyroscope (x, y, z)
- Raw sampling rate: 100.2 Hz, resampled to 60 Hz
- Columns: `timestamp, acc_x, acc_y, acc_z, gyro_x, gyro_y, gyro_z`
- Features use 2 s windows (120 samples) with 50% overlap

## Results (unseen test data)
Overall accuracy: 83.9% (sensitivity and specificity per activity are in the report).

## Videos
- Standing: [link]
- Walking: [link]
- Jumping: [link]
- Still: [link]

## How to run
1. Open `notebook/hmm_activity_recognition.ipynb` in Google Colab.
2. Put the Sensor Logger zip files in a Drive folder and set `BASE` in the first cell to that folder (the notebook was run with `/content/drive/MyDrive/HMM`).
3. Run all cells from top to bottom.
