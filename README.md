# 🎨 Stable GAN Systems: From DCGAN to CycleGAN

A complete deep learning project showcasing the evolution of Generative Adversarial Networks (GANs) — from unstable image generation to robust and controllable image translation systems.

---

## 🚀 Overview

This repository demonstrates a practical journey through three major GAN architectures:

* **DCGAN → WGAN-GP** for stable anime face generation
* **Pix2Pix** for sketch-to-color image translation
* **CycleGAN** for unpaired domain translation

The focus is on improving **training stability**, **image quality**, and **model reliability**.

---

## 🧠 Key Concepts Covered

* Mode Collapse & Training Instability
* Wasserstein Loss & Gradient Penalty
* Conditional GANs (cGANs)
* Paired vs Unpaired Image Translation
* Cycle Consistency Loss
* Domain Shift in Real-World Data

---

## 🏗️ Project Structure

```
├── dcgan_wgan_gp/
│   ├── model.py
│   ├── train.py
│   └── utils.py
│
├── pix2pix/
│   ├── generator_unet.py
│   ├── discriminator_patchgan.py
│   ├── train.py
│
├── cyclegan/
│   ├── generator_resnet.py
│   ├── discriminator.py
│   ├── train.py
│
├── datasets/
├── outputs/
├── app/
│   ├── gradio_app.py
│
└── README.md
```

---

## 🎯 Models Breakdown

### 1️⃣ DCGAN → WGAN-GP (Anime Face Generator)

**Problems with DCGAN:**

* Mode collapse
* Vanishing gradients
* Blurry outputs

**Solutions with WGAN-GP:**

* Wasserstein distance for stable gradients
* Gradient penalty instead of weight clipping
* Improved diversity and sharper images

---

### 2️⃣ Pix2Pix (Sketch Colorization)

* **Input:** Black & white sketches
* **Output:** Colored anime images
* **Architecture:** U-Net Generator + PatchGAN Discriminator

**Loss Function:**

```
Total Loss = Adversarial Loss + λ * L1 Loss
```

* L1 loss ensures structural accuracy
* PatchGAN improves local texture realism

---

### 3️⃣ CycleGAN (Unpaired Translation)

* Works without paired datasets
* Uses **cycle consistency**

**Architecture:**

* 2 Generators (A → B, B → A)
* 2 Discriminators

**Loss Components:**

* Adversarial Loss
* Cycle Consistency Loss
* Identity Loss

---

## ⚠️ Real-World Insight: Domain Shift

Models trained on rough sketches may fail on clean digital line art.

👉 Always match your **training data distribution** with real-world inputs.

---

## 💻 Installation

```bash
git clone https://github.com/your-username/stable-gan-anime-translation.git
cd stable-gan-anime-translation

pip install -r requirements.txt
```

---

## 🌐 Demo Applications

Built using **Gradio** and deployed on Hugging Face Spaces.

Anime Face Generator
https://huggingface.co/spaces/haresh8765/Anime-Face-Generator-WGANGP

Anime Sketch Colorizer
https://huggingface.co/spaces/haresh8765/pix2pix-anime-magic

CycleGAN Translator
https://huggingface.co/spaces/haresh8765/sketch-to-photo-generator-Cyclegan



---

## 📊 Evaluation Metrics

* SSIM (Structural Similarity Index)
* PSNR (Peak Signal-to-Noise Ratio)

---

## ⚡ Optimizations

* Mixed Precision Training
* Multi-GPU Support
* Efficient Memory Usage

---

## 👨‍💻 Contributors

* **Haresh Kumar**
* **Zahid Iqbal**

---

## 📌 Key Takeaway

> Improving *how* a model learns (loss functions, training strategy) is often more impactful than changing the architecture itself.

---

## 📜 License

This project is open-source and available under the MIT License.

---


