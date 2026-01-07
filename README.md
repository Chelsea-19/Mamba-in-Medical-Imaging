# Mamba-in-Medical-Imaging

# Awesome Mamba in Medical Imaging

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) 
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg)]()

> A curated list of papers, code, and resources for **Mamba (State Space Models)** applications in **Medical Imaging**.

## Introduction

**Mamba** (Selective State Space Model) has emerged as a promising alternative to CNNs and Transformers in medical image analysis. With **linear computational complexity** and **efficient long-range dependency modeling**, it addresses the bottlenecks of processing high-resolution 2D/3D medical data.

This repository corresponds to our survey paper:
**Mamba in Medical Imaging: A Comprehensive Review of the State Space Model for Efficient and Accurate Analysis** 

## Table of Contents
- [Segmentation](#segmentation)
- [Classification](#classification)
- [Detection](#detection)
- [Reconstruction](#reconstruction--enhancement)
- [Registration](#registration)
- [Generation & Multimodal](#generation)
- [Datasets](#datasets)
- [Citation](#citation)

---

<a name="segmentation"></a>
## 1. Segmentation
*Focus: 2D/3D organ segmentation, tumor segmentation, multi-organ tasks.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **VM-UNet** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.02491) | [Link](https://github.com/JCruan519/VM-UNet) | Baseline 2D Mamba-UNet integration. |
| **SegMamba** | MICCAI 2024 | [Link](https://papers.miccai.org/miccai-2024/676-Paper0663.html) | [Link](https://github.com/ge-xing/SegMamba) | 3D Mamba with Tri-orientational Spatial Scan for volumetric data. |
| **U-Mamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2401.04722) | [Link](https://github.com/bowang-lab/U-Mamba) | Hybrid CNN-Mamba architecture for general 2D/3D segmentation. |
| **nnMamba** | IEEE-ISBI 2025 | [Link](https://ieeexplore.ieee.org/abstract/document/10980694) | [Link](https://github.com/lhaof/nnMamba) | Integration of Mamba into the nnU-Net framework. |
| **Swin-UMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.03302) | [Link](https://github.com/JiarunLiu/Swin-UMamba) | Highlights ImageNet pre-training for Mamba weights. |
| **Mamba-UNet** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.05079) | [Link](https://github.com/ziyangwang007/Mamba-UNet) | Early exploration of VSS blocks in U-shape architecture. |
| **2DMamba** | CVPR 2025 | [Link](https://openaccess.thecvf.com/content/CVPR2025/html/Zhang_2DMamba_Efficient_State_Space_Model_for_Image_Representation_with_Applications_CVPR_2025_paper.html) | [Link](https://github.com/AtlasAnalyticsLab/2DMamba) | Focused on 2D segmentation tasks. |

<a name="classification"></a>
## 2. Classification
*Focus: Disease diagnosis, WSI analysis, multi-view classification.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **MedMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2403.03849) | [Link](https://github.com/YubiaoYue/MedMamba) | General purpose backbone for medical classification. |
| **MedMambaLite** | arXiv 2025 | [Link](https://arxiv.org/abs/2508.05049) | None | Lightweight version for mobile/edge devices. |
| **XFMamba** | MICCAI 2025 | [Link](https://papers.miccai.org/miccai-2025/1023-Paper1773.html) | [Link](https://github.com/XZheng0427/XFMamba) | Multi-view fusion for X-ray/MRI. |
| **GMMamba** | ICCV 2025 | [Link](https://openaccess.thecvf.com/content/ICCV2025/html/Zheng_GMMamba_Group_Masking_Mamba_for_Whole_Slide_Image_Classification_ICCV_2025_paper.html) | [Link](https://github.com/titizheng/GMMamba) | WSI analysis with position-aware mechanisms. |

<a name="detection"></a>
## 3. Detection
*Focus: Lesion detection, anomaly detection, cell detection.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **SpectMamba** | arXiv 2025 | [Link](https://arxiv.org/abs/2509.01080) | [Link](https://github.com/Tinkle01/SpectMamba) | Uses frequency domain learning for small target detection. |
| **CellMamba** | arXiv 2025 | [Link](https://github.com/ChengAoShen/CellMamba) | [Link](https://arxiv.org/abs/2512.21803) | Dense cell detection in pathology images. |
| **MambaAD** | NeurIPS 2024 | [Link](https://lewandofskee.github.io/projects/MambaAD/) | [Link](https://github.com/lewandofskee/MambaAD) | Unsupervised anomaly detection (Global + Local). |
| **SP-Mamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2404.02063) | [Link](https://github.com/JusperLee/SPMamba) | Self-supervised anomaly detection. |

<a name="reconstruction--enhancement"></a>
## 4. Reconstruction & Enhancement
*Focus: MRI acceleration, Low-dose CT denoising, Super-resolution.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **MambaRecon** | WACV 2025 | [Link](https://openaccess.thecvf.com/content/WACV2025/html/Korkmaz_MambaRecon_MRI_Reconstruction_with_Structured_State_Space_Models_WACV_2025_paper.html) | [Link](https://github.com/yilmazkorkmaz1/MambaRecon?tab=readme-ov-file) | MRI reconstruction with linear complexity (O(N)). |
| **CT-Mamba** | CMIG 2025 | [Link](https://www.sciencedirect.com/science/article/abs/pii/S0895611125001041?via%3Dihub) | [Link](https://github.com/linxuan-li/CT-Mamba?tab=readme-ov-file) | Low-dose CT denoising. |
| **DenoMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2409.13094) | [Link](https://github.com/icon-lab/DenoMamba?tab=readme-ov-file) | Image denoising framework. |
| **MMR-Mamba** | MIA 2025 | [Link](https://www.sciencedirect.com/science/article/abs/pii/S1361841525000969) | [Link](https://github.com/zoujing925/MMR-Mamba?tab=readme-ov-file) | Multi-modal MRI reconstruction. |
| **UltrasOM** | CMPB 2025 | [Link](https://www.sciencedirect.com/science/article/abs/pii/S0169260725002603?via%3Dihub) | None | Ultrasound video analysis & motion estimation. |
| **UltrasODM** | AAAI 2026 | [Link]([https://www.sciencedirect.com/science/article/abs/pii/S0169260725002603?via%3Dihub](https://arxiv.org/html/2512.07756v1)) | [Link](https://github.com/AnandMayank/UltrasODM) | Ultrasound video analysis & motion estimation. |

<a name="registration"></a>
## 5. Registration
*Focus: Deformable registration, multi-modal alignment.*

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **VMambaMorph** | arXiv 2024 | [Link](https://arxiv.org/abs/2404.05105) | [Link](https://github.com/ziyangwang007/VMambaMorph) | 3D deformable registration with cross-scan mechanism. |
| **RegMamba** | MDPI 2024 | [Link](https://www.mdpi.com/2079-9292/13/16/3305) | [Link](https://github.com/Hexu00/Regmamba) | Hybrid CNN-Mamba for large deformation handling. |
| **MambaMorph** | arXiv 2024 | [Link](https://arxiv.org/abs/2401.13934) | [Link](https://github.com/Guo-Stone/MambaMorph) | Efficient registration baseline. |
| **MambaNetLK** | arXiv 2025 | [Link](https://arxiv.org/abs/2511.00260) | [Link](https://github.com/mobarakol/MambaNetLK) | Point cloud registration for surgical navigation. |

<a name="generation"></a>
## 6. Generation & Multimodal
*Focus: Image synthesis, Cross-modality generation, Report generation.*

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **DiM** | arXiv 2024 | [Link](https://arxiv.org/abs/2405.14224) | [Link](https://github.com/tyshiwo1/DiM-DiffusionMamba) | Efficient high-res generation, replaces Attention in U-Net. |
| **I2I-Mamba** | arXiv 2024 | [Link](https://arxiv.org/html/2405.14022v4) | [Link](https://github.com/icon-lab/I2I-Mamba) | Image-to-Image translation (e.g., MRI to CT). |
| **R2Gen-Mamba** | IEEE-ISBI 2025 | [Link](https://ieeexplore.ieee.org/document/10980814) | [Link](https://github.com/YonghengSun1997/R2Gen-Mamba) | Radiology report generation. |
| **RRG-Mamba** | IJCAI 2025 | [Link](https://www.ijcai.org/proceedings/2025/824) | [Link](https://github.com/Eleanorhxd/RRG-Mamba) | Radiology report generation. |

<a name="datasets"></a>
## 💽 Key Datasets
Commonly used datasets mentioned in the review:

* **Segmentation:** [BraTS](http://braintumorsegmentation.org/) (Brain Tumor), [Synapse](https://www.synapse.org/) (Multi-organ), [MSD](http://medicaldecathlon.com/) (Medical Segmentation Decathlon), [TotalSegmentator](https://github.com/wasserth/TotalSegmentator).
* **Classification:** [CheXpert](https://stanfordmlgroup.github.io/competitions/chexpert/), [MIMIC-CXR](https://physionet.org/content/mimic-cxr/), [MedMNIST](https://medmnist.com/).
* **Detection:** [LUNA16](https://luna16.grand-challenge.org/) (Lung Nodules), [DeepLesion](https://nihcc.app.box.com/v/DeepLesion).
* **Reconstruction:** [fastMRI](https://fastmri.org/), AAPM Low Dose CT.

<a name="citation"></a>
## Citation
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
