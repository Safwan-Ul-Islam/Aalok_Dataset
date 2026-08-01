# Aalok Dataset

> 📄 **Official dataset accompanying our IEEE Access 2026 publication:**  
> **Fetal Ultrasound Monitoring Using MedSegDiff-V2–DUCKNet Ensemble Segmentation and Explainable Head Circumference Estimation**

The **Aalok Dataset** is a publicly available fetal ultrasound dataset developed to support research in automated fetal head segmentation, fetal biometric analysis, and AI-assisted prenatal healthcare. The dataset was collected from **Aalok Diagnostic & Hospital, Dhaka, Bangladesh**, and contains expert-annotated fetal head ultrasound scans covering a wide range of gestational ages.

---

## 📖 Associated Publication

This dataset is associated with the following publication:

**S. U. Islam, M. S. Saqib, M. R. Rahman and R. Khan**

**Fetal Ultrasound Monitoring Using MedSegDiff-V2–DUCKNet Ensemble Segmentation and Explainable Head Circumference Estimation**

*IEEE Access*, Volume 14, Pages 108173–108186, 2026.

🔗 **Paper:** https://doi.org/10.1109/ACCESS.2026.3712728

If you use this dataset in your research, **please cite our paper**.

---

# Dataset Overview

The Aalok Dataset was developed for semantic segmentation of fetal head ultrasound images and automated head circumference estimation using deep learning.

The dataset contains manually annotated fetal head boundaries created and verified by experienced radiologists, making it suitable for medical image segmentation, biometric estimation, explainable AI, and fetal healthcare research.

---

# Dataset Statistics

| Property | Value |
|-----------|-------|
| Imaging Modality | 2D Fetal Ultrasound |
| Total Images | **400** |
| Annotation Type | Pixel-wise Segmentation Masks |
| Image Format | PNG |
| Mask Format | PNG |
| Original Resolution | **1024 × 768** |
| Recommended Training Resolution | **256 × 256** |
| Gestational Age | **18–38 Weeks** |
| Ultrasound System | Samsung WS80A Elite |
| Annotation | Expert Manual Delineation by Radiologists |
| Application | Fetal Head Segmentation & Head Circumference Estimation |
| License | CC BY 4.0 |

---

# Dataset Features

- ✅ 400 expert-annotated fetal ultrasound images
- ✅ High-quality binary segmentation masks
- ✅ Diverse fetal orientations
- ✅ Various image qualities and shadowing conditions
- ✅ Gestational ages ranging from **18 to 38 weeks**
- ✅ Suitable for semantic segmentation research
- ✅ Suitable for medical image analysis
- ✅ Suitable for Explainable AI (XAI)
- ✅ Suitable for fetal biometric estimation

---

# Additional Dataset Metadata

The repository includes a metadata file named **`pixel_size_and_HC.csv`**, which provides image-level information for each ultrasound scan.

The CSV file contains the following columns:

| Column | Description |
|--------|-------------|
| `file_name` | Name of the ultrasound image |
| `HC_MM` | Ground-truth head circumference measurement (in millimetres) |
| `pixel_size_MM` | Pixel spacing (millimetres per pixel) used for converting pixel measurements to real-world units |

This metadata enables researchers to reproduce head circumference estimation and evaluate measurement accuracy in physical units (mm).

---

# Data Collection

The dataset was collected from **Aalok Diagnostic & Hospital, Dhaka, Bangladesh** during routine antenatal examinations using a **Samsung WS80A Elite Ultrasound System**.

Each fetal head boundary was manually annotated and independently reviewed by experienced radiologists to ensure high annotation quality.

---

# Preprocessing

The preprocessing pipeline used in our paper includes:

- Hole filling for mask refinement
- Images were symmetrically padded on both the left and right sides to preserve the original aspect ratio before resizing.
- Image resizing to **256 × 256**
- Intensity normalization
- Online data augmentation during training
- Random horizontal and vertical flipping
- Random rotation
- Random affine transformation
- Random zoom
- Gaussian noise
- Contrast adjustment

The train, validation, and test sets were generated using a **70 : 15 : 15** split before augmentation.

---

# Repository Structure

```text
Aalok_Dataset/
│
├── Aalok_Dataset/
│   ├── alk_001.png
│   ├── alk_001_mask.png
│   ├── alk_002.png
│   ├── alk_002_mask.png
│   └── .....
│
│
├── README.md
├── LICENSE
├── CITATION.cff
└── pixel_size_and_HC.csv
```

**Naming Convention**

- `alk-XXX.png` → Original fetal ultrasound image
- `alk-XXX_mask.png` → Corresponding binary segmentation mask
- `pixel_size_and_HC.csv` → Metadata containing the image filename, pixel size (mm), and ground-truth head circumference (HC) in millimetres.
---

# Citation

If you use this dataset in your research, please cite our paper.

### IEEE Citation

S. U. Islam, M. S. Saqib, M. R. Rahman and R. Khan, "Fetal Ultrasound Monitoring Using MedSegDiff-V2–DUCKNet Ensemble Segmentation and Explainable Head Circumference Estimation," *IEEE Access*, vol. 14, pp. 108173–108186, 2026, doi: **10.1109/ACCESS.2026.3712728**.

### BibTeX

```bibtex
@ARTICLE{Islam2026,
  author={Islam, Safwan Ul and Saqib, Miwan Sariana and Rahman, Md Raqibur and Khan, Riasat},
  journal={IEEE Access},
  title={Fetal Ultrasound Monitoring Using MedSegDiff-V2–DUCKNet Ensemble Segmentation and Explainable Head Circumference Estimation},
  year={2026},
  volume={14},
  pages={108173-108186},
  doi={10.1109/ACCESS.2026.3712728}
}
```
---

# License

This dataset is distributed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** License.

---


