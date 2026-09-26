# 🧠 Neuro Scanner

> **AI-powered Brain Tumor Detection Dashboard**

Neuro Scanner is an end-to-end deep learning web application that classifies brain MRI scans into one of four clinically-relevant categories — **glioma**, **meningioma**, **no tumor**, and **pituitary tumor** — with a live attention heatmap showing exactly which regions of the scan drove the prediction.

The model combines a **DenseNet121** convolutional backbone (pretrained on ImageNet and fine-tuned on MRI data) with two **CBAM (Convolutional Block Attention Module)** blocks inserted at different feature depths. This dual-attention design lets the network focus on both fine-grained local structures (early CBAM, 14×14) and whole-image semantic context (late CBAM, 7×7) — a design that consistently outperforms single-attention baselines on this task.

The application ships with a **FastAPI** inference server and a clean, medical-themed web dashboard. Upload an MRI scan, and within a second you get the predicted class, per-class confidence scores, and a Grad-CAM overlay rendered side-by-side with your original image.

---

### Why Neuro Scanner?

| | |
|---|---|
| 🎯 **Accurate** | DenseNet121 + Dual CBAM attention, trained with label smoothing and balanced class weights |
| ⚡ **Fast** | Model loaded once at server startup; each prediction takes ~200–400 ms on CPU |
| 🔍 **Explainable** | Every prediction includes a Grad-CAM heatmap — no black boxes |
| 🎨 **Clinical UI** | Clean, medical-themed dashboard built for real-world usability |
| 🐍 **Simple to run** | Two commands: `pip install -r requirements.txt` and `uvicorn backend.main:app` |
| 🚀 **Production-ready** | FastAPI backend, stateless endpoint, easy to containerize or deploy |

---

### What you can do with it

- **Researchers** — quickly triage MRI datasets and flag suspicious scans for review
- **Students** — a complete reference implementation of attention-augmented CNNs
- **Radiologists (research use)** — a second-opinion tool with visual explanations
- **Developers** — a working template for deploying medical imaging models as web apps

> ⚠️ **Not a medical device.** For research and educational use only.


---

## 👤 Author

**AMAN KUMAR RANJAN**
- Email: amankumar89669@gmail.com
- 
