# 🎵 RNN Melody Composer: AI Music Generation

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Framework](https://img.shields.io/badge/Framework-TensorFlow%202.x-orange)
![Model](https://img.shields.io/badge/Architecture-LSTM%20%2F%20RNN-green)
![Domain](https://img.shields.io/badge/Domain-Audio%20%26%20Music-purple)

## 📌 Project Overview
This project explores the creative capabilities of **Recurrent Neural Networks (RNNs)** by training a Deep Learning model to compose original Irish Folk music. 

Using a dataset of thousands of songs in **ABC notation** (a text-based music format), the model learns the temporal patterns, grammar, and structure of the music characters to generate new, never-before-heard melodies note by note.

## ⚙️ How it Works
The model treats music generation as a **Character-Level Language Modeling** task:
1.  **Input:** A sequence of characters representing musical notes (e.g., `B2GB defg`).
2.  **Processing:** An **LSTM (Long Short-Term Memory)** network processes the sequence, maintaining an internal state of the musical context.
3.  **Output:** The model predicts the probability distribution of the *next character*.
4.  **Sampling:** We sample from this distribution to generate the next note and feed it back into the model to generate the subsequent one.

## 🧠 Technical Architecture
The model is built using `tf.keras.Sequential` with the following layers:
* **Embedding Layer:** Maps each character in the vocabulary to a dense vector representation.
* **LSTM Layer:** The core recurrent layer (1024 units) that captures long-term dependencies in the melody.
* **Dense Layer:** Outputs logits for each character in the vocabulary.

## 🚀 How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/mariamashraf731/RNN-Melody-Composer.git](https://github.com/mariamashraf731/RNN-Melody-Composer.git)
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    # You also need 'abcmidi' and 'timidity' for audio conversion (sudo apt-get install abcmidi timidity)
    ```
3.  **Train & Generate:**
    Open `notebooks/Music_Generation_Lab.ipynb` and run the cells to train the model and listen to the generated output.

### The notebook includes a synthesizer to convert this text into actual audio!

## 📚 Acknowledgements
Based on the MIT 6.S191: Introduction to Deep Learning curriculum.