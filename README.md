# NST - Neural Style Transfer

> Flask web application for real-time style transfer using AdaIN PyTorch models.

[![GitHub stars](https://img.shields.io/github/stars/codedbydevansh/NST-Neural-Style-Transfer-?style=for-the-badge&logo=github)](https://github.com/codedbydevansh/NST-Neural-Style-Transfer-/stargazers) 
[![GitHub forks](https://img.shields.io/github/forks/codedbydevansh/NST-Neural-Style-Transfer-?style=for-the-badge&logo=github)](https://github.com/codedbydevansh/NST-Neural-Style-Transfer-/network/members) 
[![GitHub issues](https://img.shields.io/github/issues/codedbydevansh/NST-Neural-Style-Transfer-?style=for-the-badge&logo=github)](https://github.com/codedbydevansh/NST-Neural-Style-Transfer-/issues) 
[![Last commit](https://img.shields.io/github/last-commit/codedbydevansh/NST-Neural-Style-Transfer-?style=for-the-badge&logo=github)](https://github.com/codedbydevansh/NST-Neural-Style-Transfer-/commits/main) 
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org)

---

## 🌐 Live Demo

Experience Neural Style Transfer in real time through the deployed web application.

🔗 **[NeuralArt – AI Neural Style Transfer](https://nst-neural-style-transfer-production.up.railway.app/)**

---

## 📑 Table of Contents

- [Description](#-description)
- [Key Features](#-key-features)
- [Use Cases](#-use-cases)
- [Tech Stack](#-tech-stack)
- [Quick Start](#-quick-start)
- [Usage](#%EF%B8%8F-usage)
- [Key Dependencies](#-key-dependencies)
- [Project Structure](#-project-structure)
- [Development Setup](#-development-setup)
- [Contributors](#-contributors)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📝 Description

This project provides a functional web application and training pipeline for Neural Style Transfer (NST) using Adaptive Instance Normalization (AdaIN). It allows users to blend the content of one image with the artistic style of another, leveraging deep learning architectures to align statistical feature profiles.

---

## ✨ Key Features

- **🎨 AdaIN Style Transfer** — Implements adaptive instance normalization to align the mean and variance of content image features with those of style images.
- **🌐 Flask Web Interface** — Provides an interactive web dashboard utilizing Flask-WTF for form handling and Bootstrap for simple image upload operations.
- **💾 Pre-trained Model Support** — Loads pre-trained PyTorch weights for both the normalized VGG encoder and the final decoder network.
- **⚙️ Custom Model Training** — Includes a training script to facilitate custom training of the decoder model from scratch.

---

## 🎯 Use Cases

- Hosting a web application that lets users upload a photo and stylize it with a selected artwork theme.
- Training and fine-tuning an AdaIN decoder network with custom dataset directories.
- Experimenting with adaptive instance normalization and parameter adjustments in neural style transfer.

---

## 🛠️ Tech Stack

- **Language:** Python 🐍
- **Libraries & Frameworks:** PyTorch, TensorFlow, NumPy, Flask, Flask-WTF, Bootstrap

---

## ⚡ Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/codedbydevansh/NST-Neural-Style-Transfer-.git
cd NST-Neural-Style-Transfer-

# 2. Create & activate a virtualenv
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt
```

---

## ⚙️ Usage

### Running the Web Application
To launch the interactive local Flask server:
```bash
python app.py
```
Once started, navigate to `http://127.0.0.1:5000` in your web browser.

### Custom Model Training
To train your own AdaIN decoder model using the provided training script:
```bash
python train.py
```
<!-- TODO: Customize hyperparameters and training arguments inside train.py as needed -->

---

## 📦 Key Dependencies

```text
Flask: 3.1.2
Flask_Bootstrap: 3.3.7.1
flask_wtf: 1.2.2
numpy: 1.24,<2.0
Pillow: 12.0.0
torch: 2.2.2
torchvision: 0.17.2
tqdm: 4.66.4
Werkzeug: 3.1.4
WTForms: 3.2.1
gunicorn: latest
```

---

## 📁 Project Structure

```text
.
├── Procfile.txt
├── app.py
├── content_data
│   ├── 000000000001.jpg
│   ├── 000000000016.jpg
│   ├── 000000000019.jpg
│   ├── 000000000057.jpg
│   ├── 000000000063.jpg
│   ├── 000000000069.jpg
│   ├── 000000000080.jpg
│   ├── 000000000090.jpg
│   ├── 000000000106.jpg
│   ├── 000000000108.jpg
│   ├── 000000000128.jpg
│   ├── 000000000155.jpg
│   ├── 000000000161.jpg
│   ├── 000000000171.jpg
│   ├── 000000000178.jpg
│   ├── 000000000180.jpg
│   ├── 000000000183.jpg
│   └── 000000000188.jpg
├── decoder_final.pth
├── examples
│   ├── 1.jpg
│   ├── 100.jpg
│   ├── Tony-Stark.jpg
│   ├── stylized_Tony-Stark.jpg
│   └── stylized_Tony-Stark1.jpg
├── nixpacks.xml
├── requirements.txt
├── runtime.txt
├── static
│   └── uploads
│       ├── 1.jpg
│       ├── 10.jpg
│       ├── 100.jpg
│       ├── 1004.jpg
│       ├── 1007.jpg
│       ├── 101.jpg
│       ├── 105.jpg
│       ├── 1064.jpg
│       ├── 108.jpg
│       ├── 1097.jpg
│       ├── 11.jpg
│       ├── 12.jpg
│       ├── 125.jpg
│       ├── 1576.jpg
│       ├── 1696.jpg
│       ├── 17.jpg
│       ├── 1714.jpg
│       ├── 185.jpg
│       ├── 196.jpg
│       ├── Tony-Stark.jpg
│       ├── WIN_20250829_00_51_28_Pro.jpg
│       ├── brad_pitt.jpg
│       ├── images.jpg
│       ├── picasso_seated_nude_hr.jpg
│       ├── stylized_Tony-Stark.jpg
│       ├── stylized_WIN_20250829_00_51_28_Pro.jpg
│       ├── stylized_brad_pitt.jpg
│       └── stylized_images.jpg
├── style_data
│   ├── 1.jpg
│   ├── 10.jpg
│   ├── 11.jpg
│   ├── 12.jpg
│   ├── 14.jpg
│   ├── 16.jpg
│   ├── 17.jpg
│   ├── 18.jpg
│   └── 19.jpg
├── templates
│   └── index.html
├── train.py
├── utils
│   ├── models.py
│   └── utils.py
└── vgg_normalised.pth
```

---

## 🛠️ Development Setup

### Python Environment
1. Install Python (v3.10+ recommended)
2. Run environment setup:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install package requirements:
   ```bash
   pip install -r requirements.txt
   ```

---

## 👥 Contributors

Thanks to everyone who has contributed to this project:

<p align="left">
<a href="https://github.com/codedbydevansh" title="codedbydevansh">
  <img src="https://avatars.githubusercontent.com/u/155902353?v=4&s=64" width="64" height="64" alt="codedbydevansh" style="border-radius:50%" />
</a>
</p>

[See the full list of contributors →](https://github.com/codedbydevansh/NST-Neural-Style-Transfer-/graphs/contributors)

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Clone** your fork:
   ```bash
   git clone https://github.com/codedbydevansh/NST-Neural-Style-Transfer-.git
   ```
3. **Branch** to your feature:
   ```bash
   git checkout -b feature/your-feature
   ```
4. **Commit** your changes:
   ```bash
   git commit -m 'feat: add some feature'
   ```
5. **Push** your branch:
   ```bash
   git push origin feature/your-feature
   ```
6. **Open** a pull request

Please follow the existing code style and include tests for new behavior where applicable.

---

## 📄 License

<!-- TODO: Add License file/information (e.g. MIT, Apache 2.0) -->
This project's licensing terms have not been specified yet. Please check the repository files or contact the maintainer for more details.

---
*This README was generated with ❤️ by [ReadmeBuddy](https://readmebuddy.com)*