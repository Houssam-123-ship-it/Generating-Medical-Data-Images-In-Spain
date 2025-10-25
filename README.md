# 🧠 Medical Image Generation using GANs

This project explores the use of **Generative Adversarial Networks (GANs)** to generate synthetic **medical images** such as **X-rays** and **brain MRIs**.
The project involves **building and training a GAN**, **using pre-trained models from Medigan**, and **developing a Streamlit web app** that allows users to interactively generate medical images.
Additionally, we examine the **ethical considerations** in medical imaging AI, including bias, privacy, and fairness.

---

## 📚 Table of Contents

* [Overview](#overview)
* [Project Objectives](#project-objectives)
* [Technologies Used](#technologies-used)
* [GAN Architecture](#gan-architecture)
* [Using Pre-trained GANs (Medigan)](#using-pre-trained-gans-madigan)
* [Web Application (Streamlit)](#web-application-streamlit)
* [Ethical Considerations](#ethical-considerations)
* [Installation and Setup](#installation-and-setup)
* [Usage Instructions](#usage-instructions)
* [Key Learnings](#key-learnings)
* [References](#references)

---

## 🧩 Overview

A **Generative Adversarial Network (GAN)** is a deep learning architecture that consists of two neural networks:

* A **Generator**, which creates fake images.
* A **Discriminator**, which tries to distinguish between real and fake images.

By training these two networks together in an adversarial process, the generator learns to produce images that closely resemble real medical scans.

In this project, we:

* Train a GAN to generate **brain MRI images**.
* Use **Medigan**, a library of pre-trained medical GANs, to generate realistic medical images.
* Use **synthetic data** to train or fine-tune a classifier for medical image analysis.
* Build an interactive **Streamlit web app** for exploring GANs and generating images.

---

## 🎯 Project Objectives

### Phase 1: Build and Train a GAN

* Read in medical images (e.g., brain MRIs)
* Create the two adversarial networks:

  * **Discriminator** – distinguishes real vs. fake images
  * **Generator** – produces new, synthetic images
* Train both networks against each other
* Generate and visualize new medical images

### Phase 2: Use Pre-trained GANs (Medigan)

* Explore the **Medigan** collection of pre-trained GANs for medical imaging
* Generate synthetic datasets (e.g., X-rays, MRIs)
* Build a **data loader** for training with synthetic data
* Fine-tune a pre-trained **classification model** using GAN-generated images
* [**Click to see all Pretrained GAN models inforrmations**](Notebooks/global.json)

### Phase 3: Build the Streamlit Web App

* Design an interactive interface for users to:

  * Select different GAN models from Medigan
  * Control image generation parameters
  * Visualize generated results in real time
* Deploy the app to **Streamlit Cloud** or **GitHub Pages**

---

## ⚙️ Technologies Used

* **Python 3.x**
* **TensorFlow / PyTorch** – for building and training GANs
* **Medigan** – pre-trained GANs for medical imaging
* **Streamlit** – for building the interactive web app
* **OpenCV / PIL** – for image processing
* **Matplotlib / Seaborn** – for visualization
* **Git & GitHub** – for version control and collaboration

---

## 🧠 GAN Architecture

### 1. Generator

* Takes random noise (a **noise vector**) as input
* Produces synthetic medical images resembling real MRIs

### 2. Discriminator

* Classifies images as **real** or **fake**
* Provides feedback to the generator to improve image realism

### 3. Training Process

* The **generator** tries to fool the **discriminator**, while the discriminator learns to detect fakes.
* Over time, the generator produces increasingly realistic medical images.

---

## 🧬 Using Pre-trained GANs (Medigan)

**Medigan** is a library of **pre-trained GANs** specialized in medical imaging tasks.
It provides models that can generate:

* Brain MRIs
* Chest X-rays
* Retinal scans
* Polyp images and more

### Tasks:

* Select a GAN model from Medigan
* Generate synthetic medical data
* Use the synthetic images to **train or fine-tune** a classifier (e.g., detecting polyps or tumors)

**Benefits:**

* Helps when there’s **limited real data**
* Enables **faster model training**
* Supports **data augmentation** and **model pre-training**

---

## 🌐 Web Application (Streamlit)

We built a **Streamlit app** that allows users to:

* Choose a GAN model (e.g., MRI generator, X-ray generator)
* Adjust the number of images to generate
* View generated medical images directly in the browser

### Example Features:

* Sidebar controls for GAN selection
* Adjustable noise seed and number of outputs
* Real-time image display grid
* Download option for generated images

---

## ⚖️ Ethical Considerations

### 🩺 Ethics in Computer Vision:

**The Quest to Develop Fair and Ethical Algorithms in Medical Imaging**

As AI becomes more integrated into healthcare, developers must address **bias**, **privacy**, and **environmental impact**.

From the article by the **National Institute of Biomedical Imaging and Bioengineering (NIBIB):**

> “Bias can sneak into an AI model in multiple different ways—from the data used to develop it to how it’s tested and deployed. An algorithm trained primarily on one population may not perform well on another.”

### Common Sources of Bias:

* **Demographic bias** – Models trained on data from one ethnic group may fail on others.
* **Temporal bias** – Outdated data may no longer represent current patient populations.
* **Data leakage** – Using the same patients for both training and testing reduces generalizability.

### Mitigation Strategies:

* Use **diverse and representative datasets**
* Perform **bias audits** during model development
* Re-evaluate models regularly with new data
* Use tools like **MIDRC’s bias awareness tool** to identify and mitigate bias

Ethical AI in medical imaging ensures fairness, trust, and improved patient outcomes.

---

## 🧰 Installation and Setup

```bash
# 1. Clone this repository
git clone https://github.com/Houssam-123-ship-it/Generating-Medical-Data-Images-In-Spain

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the Streamlit app
streamlit run app.py
```

---

## ▶️ Usage Instructions

1. Launch the app with `streamlit run app.py`
2. Select a GAN model from the sidebar
3. Adjust generation parameters (e.g., number of images)
4. Click **Generate**
5. View, download, or save the synthetic medical images

---

## 💡 Key Learnings

* GANs can generate realistic medical images for research and data augmentation
* Synthetic data can help train models when real data is scarce
* Streamlit provides a powerful, simple way to build interactive AI tools
* Ethical awareness is critical in deploying AI models in healthcare
* Bias can appear at every stage of the ML pipeline, and must be continuously monitored

---

## 📚 References

* **Medigan: Pre-trained GANs for Medical Imaging**
  [https://github.com/Project-Medigan](https://github.com/Project-Medigan)

* **The Quest to Develop Fair and Ethical Algorithms in Medical Imaging**
  National Institute of Biomedical Imaging and Bioengineering
  [https://www.nibib.nih.gov/news-events/newsroom/quest-develop-fair-and-ethical-algorithms-medical-imaging](https://www.nibib.nih.gov/news-events/newsroom/quest-develop-fair-and-ethical-algorithms-medical-imaging)

* **Goodfellow et al., 2014 — Generative Adversarial Nets**
  [https://arxiv.org/abs/1406.2661](https://arxiv.org/abs/1406.2661)


