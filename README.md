# Mamba-in-Medical-Imaging

# Awesome Mamba in Medical Imaging

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) 
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg)]()

> A curated list of papers, code, and resources for **Mamba (State Space Models)** applications in **Medical Imaging**.

## 📖 Introduction

**Mamba** (Selective State Space Model) has emerged as a promising alternative to CNNs and Transformers in medical image analysis. [cite_start]With **linear computational complexity** and **efficient long-range dependency modeling**, it addresses the bottlenecks of processing high-resolution 2D/3D medical data [cite: 4-5].

This repository corresponds to our survey paper:
[cite_start]**Mamba in Medical Imaging: A Comprehensive Review of the State Space Model for Efficient and Accurate Analysis** [cite: 1-2]

## 📝 Change Log
* **[202X-XX-XX]** Initial release of the Awesome List based on our survey.

## 📚 Table of Contents
- [Segmentation](#segmentation)
- [Classification](#classification)
- [Detection](#detection)
- [Reconstruction & Enhancement](#reconstruction--enhancement)
- [Registration](#registration)
- [Generation](#generation)
- [Datasets](#datasets)
- [Citation](#citation)

---

<a name="segmentation"></a>
## 1. Segmentation
[cite_start]*Focus: 2D/3D organ segmentation, tumor segmentation, multi-organ tasks.* [cite: 100-104]

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **VM-UNet** | arXiv 2024 | [Link]() | [Link]() | [cite_start]Baseline 2D Mamba-UNet integration[cite: 6]. |
| **SegMamba** | MICCAI 2024 | [Link]() | [Link]() | [cite_start]3D Mamba with Tri-orientational Spatial Scan for volumetric data[cite: 122]. |
| **U-Mamba** | arXiv 2024 | [Link]() | [Link]() | [cite_start]Hybrid CNN-Mamba architecture for general 2D/3D segmentation[cite: 133]. |
| **nnMamba** | arXiv 2024 | [Link]() | [Link]() | [cite_start]Integration of Mamba into the nnU-Net framework[cite: 135]. |
| **Swin-UMamba** | arXiv 2024 | [Link]() | [Link]() | [cite_start]Highlights ImageNet pre-training for Mamba weights[cite: 134]. |
| **Mamba-UNet** | - | [Link]() | [Link]() | [cite_start]Early exploration of VSS blocks in U-shape architecture[cite: 6]. |
| **2DMamba** | - | [Link]() | [Link]() | [cite_start]Focused on 2D segmentation tasks[cite: 6]. |

<a name="classification"></a>
## 2. Classification
[cite_start]*Focus: Disease diagnosis, WSI analysis, multi-view classification.* [cite: 138-143]

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **MedMamba** | - | [Link]() | [Link]() | [cite_start]General purpose backbone for medical classification[cite: 147]. |
| **MedMambaLite** | - | [Link]() | [Link]() | [cite_start]Lightweight version for mobile/edge devices[cite: 148]. |
| **XFMamba** | - | [Link]() | [Link]() | [cite_start]Multi-view fusion for X-ray/MRI[cite: 150]. |
| **M3amba** | - | [Link]() | [Link]() | [cite_start]For Whole Slide Imaging (WSI), handles ultra-long sequences[cite: 160]. |
| **GMMamba** | - | [Link]() | [Link]() | [cite_start]WSI analysis with position-aware mechanisms[cite: 162]. |

<a name="detection"></a>
## 3. Detection
[cite_start]*Focus: Lesion detection, anomaly detection, cell detection.* [cite: 165-169]

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **SpectMamba** | - | [Link]() | [Link]() | [cite_start]Uses frequency domain learning for small target detection[cite: 179]. |
| **CellMamba** | - | [Link]() | [Link]() | [cite_start]Dense cell detection in pathology images[cite: 183]. |
| **MambaAD** | - | [Link]() | [Link]() | [cite_start]Unsupervised anomaly detection (Global + Local)[cite: 189]. |
| **SP-Mamba** | - | [Link]() | [Link]() | [cite_start]Self-supervised anomaly detection[cite: 189]. |

<a name="reconstruction--enhancement"></a>
## 4. Reconstruction & Enhancement
[cite_start]*Focus: MRI acceleration, Low-dose CT denoising, Super-resolution.* [cite: 193-199]

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **MambaRecon** | - | [Link]() | [Link]() | [cite_start]MRI reconstruction with linear complexity (O(N))[cite: 208]. |
| **CT-Mamba** | - | [Link]() | [Link]() | [cite_start]Low-dose CT denoising[cite: 210]. |
| **DenoMamba** | - | [Link]() | [Link]() | [cite_start]Image denoising framework[cite: 210]. |
| **MMR-Mamba** | - | [Link]() | [Link]() | [cite_start]Multi-modal MRI reconstruction[cite: 215]. |
| **UltrasOM** | - | [Link]() | [Link]() | [cite_start]Ultrasound video analysis & motion estimation[cite: 220]. |

<a name="registration"></a>
## 5. Registration
[cite_start]*Focus: Deformable registration, multi-modal alignment.* [cite: 223-228]

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **VMambaMorph** | - | [Link]() | [Link]() | [cite_start]3D deformable registration with cross-scan mechanism[cite: 243]. |
| **RegMamba** | - | [Link]() | [Link]() | [cite_start]Hybrid CNN-Mamba for large deformation handling[cite: 237]. |
| **MambaMorph** | - | [Link]() | [Link]() | [cite_start]Efficient registration baseline[cite: 242]. |
| **MambaNetLK** | - | [Link]() | [Link]() | [cite_start]Point cloud registration for surgical navigation[cite: 248]. |

<a name="generation"></a>
## 6. Generation
[cite_start]*Focus: Image synthesis, Cross-modality generation, Report generation.* [cite: 253-257]

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Diffusion Mamba (DiM)** | arXiv 2024 | [Link]() | [Link]() | [cite_start]Efficient high-res generation, replaces Attention in U-Net[cite: 271]. |
| **I2I-Mamba** | - | [Link]() | [Link]() | [cite_start]Image-to-Image translation (e.g., MRI to CT)[cite: 277]. |
| **R2Gen-Mamba** | - | [Link]() | [Link]() | [cite_start]Radiology report generation[cite: 283]. |
| **RRG-Mamba** | IJCAI 2025 | [Link]() | [Link]() | [cite_start]Radiology report generation[cite: 283]. |

<a name="datasets"></a>
## 💽 Key Datasets
[cite_start]Commonly used datasets mentioned in the review [cite: 435-547]:

* [cite_start]**Segmentation:** [BraTS](http://braintumorsegmentation.org/) (Brain Tumor) [cite: 441][cite_start], [Synapse](https://www.synapse.org/) (Multi-organ) [cite: 550][cite_start], [MSD](http://medicaldecathlon.com/) (Medical Segmentation Decathlon) [cite: 441][cite_start], [TotalSegmentator](https://github.com/wasserth/TotalSegmentator)[cite: 447].
* [cite_start]**Classification:** [CheXpert](https://stanfordmlgroup.github.io/competitions/chexpert/) [cite: 464][cite_start], [MIMIC-CXR](https://physionet.org/content/mimic-cxr/) [cite: 464][cite_start], [MedMNIST](https://medmnist.com/)[cite: 470].
* [cite_start]**Detection:** [LUNA16](https://luna16.grand-challenge.org/) (Lung Nodules) [cite: 488][cite_start], [DeepLesion](https://nihcc.app.box.com/v/DeepLesion)[cite: 490].
* [cite_start]**Reconstruction:** [fastMRI](https://fastmri.org/) [cite: 510][cite_start], AAPM Low Dose CT[cite: 511].

<a name="citation"></a>
## ✏️ Citation
If you find this repository or our survey useful, please consider citing our paper:

```bibtex
@article{YourName2025MambaSurvey,
  title={Mamba in Medical Imaging: A Comprehensive Review of the State Space Model for Efficient and Accurate Analysis},
  author={Your Name and Co-Authors},
  journal={Journal/Conference Name},
  year={2025},
  publisher={Publisher}
}
```

## 🤝 Contribution

We welcome and appreciate all contributions to keep this list up-to-date!

If you have a **new paper** or **code repository** relevant to Mamba in Medical Imaging, please feel free to contribute:

### 🔹 How to Submit
1.  **Fork** this repository.
2.  Create a new branch (e.g., `feature/add-new-paper`).
3.  Add the paper/code information to the corresponding section (e.g., Segmentation, Classification).
4.  Submit a **Pull Request (PR)**.

### 🔹 Format Guide
Please follow the existing table format to ensure consistency:

```markdown
| **Model Name** | Publication | [Paper Title](Link) | [Code](Link) | Key Description |
| **SegMamba** | MICCAI 2024 | [SegMamba: Long-range Sequential Modeling...](https://arxiv.org/abs/xxxx) | [GitHub](https://github.com/xxxx) | 3D Mamba with Tri-orientational Spatial Scan. |
```
