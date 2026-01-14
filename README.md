<div align="center">

---
### **System for Supporting Brain Cancer Diagnosis**  
</div>

---

# **Project: Development of models and software with artificial intelligence and machine learning to support decision-making in cancer diagnosis and treatment**


This work reflects independent research and engineering experience.
It does not include proprietary source code, confidential information, or client-specific implementations.

> **Portfolio Documentation** - For inquiries about implementation, architecture consultation, or collaboration: **remihuro@hotmail.com**

# 🧠 Medical System (Cranius AI) - AI-Assisted Segmentation and Diagnosis Platform

Prediction, segmentation, and explainability system for brain cancer diagnosis, developed as part of the research project at the **Universidad Politécnica Salesiana of Cuenca-Ecuador**.

## 📌 Description

This system allows doctors and healthcare professionals to upload medical images (T1, T1c, T2, and FLAIR modalities), perform automatic segmentations with artificial intelligence models (such as `nnU-Net`), visualize comparisons with manual segmentations, generate visual explanations (Grad-CAM), and produce clinical reports in PDF format.

## Video demonstration: cancer-ai-support-platform:
   [![OmniBot Medium Demo](https://img.youtube.com/vi/EsHTz5RE8dw/maxresdefault.jpg)](https://youtu.be/EsHTz5RE8dw)

---

## ⚙️ Technologies Used

- **Backend**: FastAPI + SQLAlchemy + PostgreSQL
- **Frontend**: Angular + TailwindCSS
- **Deep Learning**: nnU-Net (v1), PyTorch
- **Visualization**: Plotly, Matplotlib
- **Image Storage**: NIfTI (.nii.gz)
- **Reports**: Embedded HTML + `pdfkit` + `wkhtmltopdf`
- **Additional scraping (optional)**: Selenium, BeautifulSoup

---

## 📂 Project Structure

```bash
Medical-System/
├── backend/
│   ├── main.py
│   ├── routers/
│   ├── services/
│   ├── models/
│   ├── utils/
│   └── static/
├── frontend/
│   └── src/
│       └── app/
│           ├── components/
│           ├── pages/
│           └── services/
├── nnUNet_raw/
├── nnUNet_results/
├── scripts/
├── requirements.txt
└── README.md
```

---

## 🚀 Main Features

- [x] Upload of medical modalities (T1, T1c, T2, FLAIR)
- [x] Automatic segmentation with `nnU-Net`
- [x] Interactive visualization and Grad-CAM
- [x] Comparison with manual segmentation
- [x] Clinical PDF reports
- [x] User registration and authentication
- [x] Manual evaluation logging
- [x] Surveys to assess AI usefulness

---

## 🧪 Model Training

The model was trained on the **BraTS 2023 (ASNR-MICCAI)** dataset using `nnU-Net v1`.

To train with two modalities (for example, T1 and T1c), the following configuration was used:

```bash
nnUNet_plan_and_preprocess -t 501 --verify_dataset_integrity
nnUNet_train 2d nnUNetTrainerV2 501 0 --npz
```

> The data is organized in `nnUNet_raw/Task501_BrainTumour/` following the official format.

---

## 📄 Report Generation

Each patient has a unique folder (`YYYY-MM-DD_patient_id`) where the following files are stored:

- `segmentation_summary.png`
- `class_distribution.png`
- `report.html`
- `report.pdf`

---

## 🩺 Clinical Applications

- Support for brain tumor diagnosis
- Automatic vs. manual visual evaluation
- Full traceability per patient
- Statistical record of usage and medical feedback

---

## 🔒 Authentication and Permissions

The system allows authenticated user roles (doctor) for full access to patient modules, reports, image uploads, and AI evaluation.

---

## 📚 References

- [nnU-Net: Official Framework](https://github.com/MIC-DKFZ/nnUNet)
- [BraTS 2023 Dataset](https://www.synapse.org/#!Synapse:syn51068140)
- [FastAPI Docs](https://fastapi.tiangolo.com/)
- [3D Slicer](https://www.slicer.org/)

---

## 👨‍⚕️ Authors:

**Team Lead, AI Engineer, Software Engineer and Full Stack Developer: Remigio Hurtado**

**AI Developers and Full Stack Developers: Leonardo Crespo, Carlos Saico, Paul Sigua, David Alvarado, Jeyson Pañora, Diego Tapia**

---

### 🔒 Production Source Code

The **complete production codebase** (services, logic, database controllers, etc.) is **proprietary and not publicly available**.

### 🤝 Collaboration Opportunities

**The production system is available through:**
- Custom implementation for enterprise clients
- Architecture consulting and technical advisory
- Licensing agreements for commercial deployment
- Integration partnerships and white-label solutions
- Direct employment opportunities

**For inquiries:**
- 🏢 Enterprise integration and custom implementations
- 💼 Technical consulting engagements
- 🔧 Code review and architecture assessment
- 📋 Licensing and partnership discussions
- 💻 Full-time or contract opportunities

📩 **Contact:** remihuro@hotmail.com

---

## 📃 License

All rights to the medical models and data used belong to their original authors.

*This project was carried out with the approval of an Ethics Committee and based on the acquisition of anonymized data.*
