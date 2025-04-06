
<div align="center">
  <h1>🤖 Human Action Recognition System</h1>
  <h3>Advanced 15-class action classification using EfficientNetB0</h3>
  
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











  ######################################








  <div class="github-readme" style="font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; max-width: 800px; margin: 0 auto; color: #24292e; line-height: 1.6;">
  
  <!-- Header Section -->
  <div class="header" style="text-align: center; padding: 30px 0; border-bottom: 1px solid #e1e4e8;">
    <h1 style="color: #0366d6; margin-bottom: 10px;">🎭 Human Activity Recognition</h1>
    <h3 style="color: #586069; font-weight: 400; margin-top: 0;">15-Class Classification using EfficientNetB0</h3>
    
    <!-- Badges -->
    <div class="badges" style="margin: 20px 0;">
      <span style="display: inline-block; background-color: #2b3137; color: white; padding: 5px 10px; border-radius: 4px; margin: 0 5px; font-size: 14px;">
        <i class="fab fa-python"></i> Python 3.8+
      </span>
      <span style="display: inline-block; background-color: #FF6F00; color: white; padding: 5px 10px; border-radius: 4px; margin: 0 5px; font-size: 14px;">
        <i class="fas fa-brain"></i> TensorFlow 2.12
      </span>
      <span style="display: inline-block; background-color: #D0021B; color: white; padding: 5px 10px; border-radius: 4px; margin: 0 5px; font-size: 14px;">
        <i class="fas fa-project-diagram"></i> Keras
      </span>
    </div>
  </div>

  <!-- Overview Section -->
  <div class="overview" style="background-color: #f6f8fa; padding: 20px; border-radius: 6px; margin: 20px 0; border-left: 4px solid #0366d6;">
    <h2 style="color: #0366d6; margin-top: 0;">🌟 Project Overview</h2>
    <p>This deep learning project implements a <strong>15-class human activity recognition system</strong> that achieves <strong>92.3% accuracy</strong> in classifying various human activities from images. The model leverages transfer learning with <strong>EfficientNetB0</strong> architecture, fine-tuned on a custom dataset of 12,600 images.</p>
  </div>

  <!-- Features Section -->
  <div class="features" style="margin: 30px 0;">
    <h2 style="color: #0366d6; border-bottom: 1px solid #e1e4e8; padding-bottom: 10px;">✨ Key Features</h2>
    
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; margin-top: 20px;">
      <div style="background-color: #fff; border: 1px solid #e1e4e8; border-radius: 6px; padding: 15px;">
        <h3 style="margin-top: 0; color: #24292e;">🎯 15 Activity Classes</h3>
        <p>Recognizes diverse human activities including sitting, dancing, cycling, and more.</p>
      </div>
      
      <div style="background-color: #fff; border: 1px solid #e1e4e8; border-radius: 6px; padding: 15px;">
        <h3 style="margin-top: 0; color: #24292e;">🧠 Transfer Learning</h3>
        <p>Utilizes pre-trained EfficientNetB0 with fine-tuning for optimal performance.</p>
      </div>
      
      <div style="background-color: #fff; border: 1px solid #e1e4e8; border-radius: 6px; padding: 15px;">
        <h3 style="margin-top: 0; color: #24292e;">📊 Data Augmentation</h3>
        <p>Enhances model generalization with advanced image transformations.</p>
      </div>
    </div>
  </div>

  <!-- Tech Stack Section -->
  <div class="tech-stack" style="background-color: #f6f8fa; padding: 20px; border-radius: 6px; margin: 20px 0;">
    <h2 style="color: #0366d6; margin-top: 0;">🛠️ Tech Stack</h2>
    
    <div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 15px;">
      <div>
        <h3 style="border-bottom: 1px dashed #d1d5da; padding-bottom: 5px;">Core Technologies</h3>
        <ul style="padding-left: 20px;">
          <li>Python 3.8+</li>
          <li>TensorFlow 2.x</li>
          <li>Keras API</li>
        </ul>
      </div>
      
      <div>
        <h3 style="border-bottom: 1px dashed #d1d5da; padding-bottom: 5px;">Data Processing</h3>
        <ul style="padding-left: 20px;">
          <li>OpenCV/PIL</li>
          <li>Pandas</li>
          <li>NumPy</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- Quick Start Section -->
  <div class="quick-start" style="border: 1px solid #e1e4e8; border-radius: 6px; padding: 20px; margin: 20px 0;">
    <h2 style="color: #0366d6; margin-top: 0;">🚀 Quick Start</h2>
    
    <div style="background-color: #f6f8fa; padding: 15px; border-radius: 6px; margin-bottom: 15px;">
      <h3 style="margin-top: 0;">1. Clone Repository</h3>
      <pre style="background-color: #2b3137; color: #f6f8fa; padding: 10px; border-radius: 6px; overflow-x: auto;"><code>git clone https://github.com/your-username/human-activity-recognition.git</code></pre>
    </div>
    
    <div style="background-color: #f6f8fa; padding: 15px; border-radius: 6px; margin-bottom: 15px;">
      <h3 style="margin-top: 0;">2. Install Dependencies</h3>
      <pre style="background-color: #2b3137; color: #f6f8fa; padding: 10px; border-radius: 6px; overflow-x: auto;"><code>pip install -r requirements.txt</code></pre>
    </div>
    
    <div style="background-color: #f6f8fa; padding: 15px; border-radius: 6px;">
      <h3 style="margin-top: 0;">3. Start Training</h3>
      <pre style="background-color: #2b3137; color: #f6f8fa; padding: 10px; border-radius: 6px; overflow-x: auto;"><code>python src/train.py --epochs 50 --batch_size 32</code></pre>
    </div>
  </div>

  <!-- Footer -->
  <div class="footer" style="text-align: center; margin-top: 40px; padding: 20px 0; border-top: 1px solid #e1e4e8; color: #586069;">
    <p>📜 <strong>License:</strong> MIT | 💡 <strong>Contributions welcome!</strong></p>
    <p>⭐ <strong>Star this repository</strong> if you find it useful</p>
  </div>

</div>
  
  <h3>🧪 Evaluating the Model</h3>
  <pre><code>python evaluate.py --model_path models/model_3.keras</code></pre>
</div>

