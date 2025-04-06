
<div align="center">
  <h1>🤖 Human Action Recognition System</h1>
  <h3>Advanced 15-class activity classification using EfficientNetB0</h3>
  
  <p align="center">
    <img src="https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge" alt="Python">
    <img src="https://img.shields.io/badge/TensorFlow-2.12-orange?style=for-the-badge" alt="TensorFlow">
    <img src="https://img.shields.io/badge/Keras-DD0031?style=for-the-badge" alt="Keras">
    <img src="https://img.shields.io/badge/Accuracy-92.3%25-green?style=for-the-badge" alt="Accuracy">
    <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" alt="License">
  </p>
</div>

<div style="background-color: #f8f9fa; padding: 20px; border-radius: 10px; border-left: 5px solid #6c757d;">
  <p>This project implements a <strong>15-class human action recognition system</strong> using transfer learning with <strong>EfficientNetB0</strong>. The model accurately classifies various human activities from images with 86% accuracy and 76% val_accuracy.</p>
</div>

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 15px; margin: 20px 0;">
  <div style="background-color: #e9ecef; padding: 15px; border-radius: 8px;">
    <h4>📦 Data Statistics</h4>
    <ul>
      <li>Total images: 12,600</li>
      <li>Image dimensions: 224×224×3</li>
      <li>Training samples: 10,080 (80%)</li>
      <li>Test samples: 2,520 (20%)</li>
    </ul>
  </div>
  
  <div style="background-color: #e9ecef; padding: 15px; border-radius: 8px;">
    <h4>🏷️ Activity Classes</h4>
    <div style="columns: 2;">
      <ul>
        <li>sitting</li>
        <li>using_laptop</li>
        <li>hugging</li>
        <li>sleeping</li>
        <li>drinking</li>
        <li>clapping</li>
        <li>dancing</li>
      </ul>
      <ul>
        <li>cycling</li>
        <li>calling</li>
        <li>laughing</li>
        <li>eating</li>
        <li>fighting</li>
        <li>listening_to_music</li>
        <li>running</li>
        <li>texting</li>
      </ul>
    </div>
  </div>
</div>

<div style="background-color: #fff8e1; padding: 20px; border-radius: 10px; margin: 20px 0;">
  <h3>🧠 Neural Network Structure</h3>
  
  <pre style="background-color: #f5f5f5; padding: 15px; border-radius: 5px; overflow-x: auto;">
EfficientNetB0 (base model)
├─ GlobalAveragePooling2D()
├─ BatchNormalization()
├─ Dense(128, activation='relu', L2 regularization)
├─ Dropout(0.5)
├─ Dense(128, activation='relu')
├─ Dropout(0.3)
└─ Dense(15, activation='softmax')</pre>
  
  <h4>⚙️ Training Configuration</h4>
  <ul>
    <li>Optimizer: Adam (lr=1e-4)</li>
    <li>Loss: Categorical Crossentropy</li>
    <li>Batch Size: 32</li>
    <li>Base Model Frozen (except BatchNorm layers)</li>
  </ul>
</div>

<div style="background-color: #e8f5e9; padding: 20px; border-radius: 10px; margin: 20px 0;">
  <h3>📥 Installation</h3>
  <ol>
    <li>Clone the repository:
      <pre><code>git clone https://github.com/your-username/15-Class-CNN-Classifier.git</code></pre>
    </li>
    <li>Install dependencies:
      <pre><code>pip install -r requirements.txt</code></pre>
    </li>
    <li>Download dataset from <a href="[Data](https://www.kaggle.com/datasets/meetnagadia/human-action-recognition-har-dataset)">Kaggle</a> and place in <code>Data/</code> directory</li>
  </ol>
  
  <h3>🏋️ Training the Model</h3>
  <pre><code>python train.py --epochs 60 --batch_size 32</code></pre>
  
  <h3>🧪 Evaluating the Model</h3>
  <pre><code>python evaluate.py --model_path models/model_3.keras</code></pre>
</div>

