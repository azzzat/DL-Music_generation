# 🎵 MIDI Music Generation with LSTM

## 📝 Overview
This project explores the use of deep learning techniques for generating music using LSTM-based neural networks. The model is trained on MIDI files of classical music and learns to generate harmonic musical sequences based on patterns found in the training data.

## ✨ Features
- 📂 **MIDI Data Processing**: Extracts and analyzes musical sequences from MIDI files.
- 🎼 **Chord Normalization**: Simplifies and standardizes chord representations.
- 📊 **Data Visualization**: Plots distributions of composers and chord frequencies.
- 🤖 **LSTM-based Model**: Sequential neural network designed for sequence prediction.
- 🎶 **Music Generation**: Generates new musical compositions based on learned patterns.
- 🔊 **MIDI to Audio Conversion**: Uses FluidSynth to convert generated MIDI files to playable audio.

## ⚙️ Installation
### 📌 Prerequisites
Ensure you have Python installed and the following dependencies:

```bash
pip install numpy pandas seaborn matplotlib tensorflow keras music21 tqdm fluidsynth
```

## 🚀 Usage
### 📥 1. Prepare Dataset
- Place MIDI files in the dataset directory.
- The script collects file paths and organizes them into a Pandas DataFrame.

### 🎼 2. Preprocess Data
- Normalize note durations using `round_chord_durations`.
- Filter out rare chords to focus on frequently used ones.


🔧 **Hyperparameters:**
- 📏 `BATCH_SIZE = 32` – Number of sequences processed per step.
- 🔁 `NUM_EPOCHS = 90` – Total training iterations over the dataset.
- 🎵 `SEQUENCE_LENGTH = 64` – Number of notes in each input sequence.

## 🏗️ 3. Model Architecture
The model consists of:
- 🧠 **LSTM Layers** (512 and 256 units) to learn sequential dependencies.
- 🚫 **Dropout Layers** (0.2) to prevent overfitting.
- 🔢 **Dense Layers** (256 → 128 → Output) with ReLU activation.
- 📊 **Softmax Output Layer** to predict the next chord in the sequence.
- ⚡ **Adam Optimizer** with a learning rate of `0.0005`.

## 📈 Results
- ✅ The model successfully generates MIDI compositions that follow the harmonic structures of the training dataset.
- 📊 Visualization of chord distributions helps in understanding common patterns in classical music.

## 🎧 Sample Generated Music
You can listen to a sample generated melody here:
https://github.com/user-attachments/assets/1c138f27-6838-4113-a5ba-c2d1c6c1ceda

yep:
<video src="https://github.com/user-attachments/assets/1c138f27-6838-4113-a5ba-c2d1c6c1ceda" width="300" />


## 🔮 Future Improvements
- 🎷 Train on a more diverse dataset including jazz and pop music.
- 🎯 Implement attention mechanisms for improved sequence modeling.
- 🏗️ Experiment with different architectures such as Transformer-based models.

## 🙌 Acknowledgments
This project utilizes open-source datasets from Kaggle and libraries like TensorFlow, Keras, and Music21.

## 📜 License
This project is licensed under the MIT License.
