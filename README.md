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
- [Fundation](#fundation)
- [Segmentation](#segmentation)
- [Classification](#classification)
- [Detection](#detection)
- [Reconstruction](#reconstruction--enhancement)
- [Registration](#registration)
- [Generation & Multimodal](#generation)
- [Review Papers](#reviews)
- [Datasets](#datasets)
- [Citation](#citation)

---
<a name="fundation"></a>
## 0. Fundation Models
*Focus: The original theoretical foundations and vision backbones.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **HiPPO** | NeurIPS 2020 | [Link](https://arxiv.org/abs/2008.07669) | [Link](https://github.com/HazyResearch/hippo-code) | **[Precursor]** Recurrent Memory with Optimal Polynomial Projections; the math theory behind S4/Mamba. |
| **S4** | NeurIPS 2021 | [Link](https://arxiv.org/abs/2111.00396) | [Link](https://github.com/HazyResearch/state-spaces) | **[Precursor]** Structured State Spaces for Long-Range Sequence Modeling; the first efficient SSM. |
| **Mamba** | arXiv 2023 | [Link](https://arxiv.org/abs/2312.00752) | [Link](https://github.com/state-spaces/mamba) | **[Foundation]** The original Selective State Space Model with linear complexity. |
| **VMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2401.10166) | [Link](https://github.com/MzeroMiko/VMamba) | **[Vision Backbone]** Visual State Space Model with 2D Selective Scan (SS2D). |
| **Vim** | ICML 2024 | [Link](https://arxiv.org/abs/2401.09417) | [Link](https://github.com/hustvl/Vim) | **[Vision Backbone]** Vision Mamba; bidirectional blocks for visual representation. |


<a name="segmentation"></a>
## 1. Segmentation
*Focus: 2D/3D organ segmentation, tumor segmentation, multi-organ tasks.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **VM-UNet** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.02491) | [Link](https://github.com/JCruan519/VM-UNet) | Baseline 2D Mamba-UNet integration. |
| **U-Mamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2401.04722) | [Link](https://github.com/bowang-lab/U-Mamba) | Hybrid CNN-Mamba architecture for general 2D/3D segmentation. |
| **Swin-UMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.03302) | [Link](https://github.com/JiarunLiu/Swin-UMamba) | Highlights ImageNet pre-training for Mamba weights. |
| **Mamba-UNet** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.05079) | [Link](https://github.com/ziyangwang007/Mamba-UNet) | Early exploration of VSS blocks in U-shape architecture. |
| **LMa-UNet** | arXiv 2024 | [Link](https://arxiv.org/html/2403.07332v1) | [Link](https://github.com/NimoXW/LMa-UNet) | Global modeling capability is superior to self-attention mechanism. |
| **LightM-UNet** | arXiv 2024 | [Link](https://arxiv.org/abs/2403.05246) | [Link](https://github.com/MrBlankness/LightM-UNet) | Extremely lightweight design. |
| **UltraLight VM-UNet** | arXiv 2024 | [Link](https://arxiv.org/html/2403.20035v1) | [Link](https://github.com/wurenkai/UltraLight-VM-UNet) | While maintaining high performance, the parameters are significantly reduced. |
| **Weak-Mamba-UNet** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.10887) | [Link](https://github.com/ziyangwang007/Weak-Mamba-UNet) | Collaborative cross-supervision mechanisms enhance the performance of weak supervision. |
| **ProMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2403.13660) | \ | Prompt-Mamba for polyp segmentation. |
| **SegMamba** | MICCAI 2024 | [Link](https://papers.miccai.org/miccai-2024/676-Paper0663.html) | [Link](https://github.com/ge-xing/SegMamba) | 3D Mamba with Tri-orientational Spatial Scan for volumetric data. |
| **2DMamba** | CVPR 2025 | [Link](https://openaccess.thecvf.com/content/CVPR2025/html/Zhang_2DMamba_Efficient_State_Space_Model_for_Image_Representation_with_Applications_CVPR_2025_paper.html) | [Link](https://github.com/AtlasAnalyticsLab/2DMamba) | Focused on 2D segmentation tasks. |
| **nnMamba** | IEEE-ISBI 2025 | [Link](https://ieeexplore.ieee.org/abstract/document/10980694) | [Link](https://github.com/lhaof/nnMamba) | Integration of Mamba into the nnU-Net framework. |
| **Mamba-Sea** | IEEE-TMI 2025 | [Link](https://ieeexplore.ieee.org/document/10980210) | [Link](https://github.com/orange-czh/Mamba-Sea/blob/main/README.md) | A "Global-to-Local" sequence enhancement mechanism is proposed. |
| **Vivim** | IEEE-TCSVT 2025 | [Link](https://ieeexplore.ieee.org/document/10973086) | [Link](https://github.com/scott-yjyang/Vivim) | The effectiveness in medical video segmentation was verified. |
| **TIFCMamba** | MICCAI 2025 | [Link](https://link.springer.com/chapter/10.1007/978-3-032-04984-1_29) | [Link](https://github.com/PZalio/TIFCMamba) | Using text descriptions to assist image segmentation. |
| **H-vmunet** | NEUCOM 2025 | [Link](https://www.sciencedirect.com/science/article/abs/pii/S0925231225001195?via%3Dihub) | [Link](https://github.com/wurenkai/H-vmunet) | High-order Vision Mamba UNet for Medical Image Segmentation. |


<a name="classification"></a>
## 2. Classification
*Focus: Disease diagnosis, WSI analysis, multi-view classification.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **MedMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2403.03849) | [Link](https://github.com/YubiaoYue/MedMamba) | General purpose backbone for medical classification. |
| **CMViM** | arXiv 2024 | [Link](https://arxiv.org/abs/2403.16520) | \ | Contrastive learning aligns multimodal representations. |
| **MamMIL** | IEEE-BIBM 2024 | [Link](https://ieeexplore.ieee.org/abstract/document/10822552) | [Link](https://github.com/Vison307/MamMIL) | Less GPU memory & Better than Transformer-based method. |
| **MedMambaLite** | arXiv 2025 | [Link](https://arxiv.org/abs/2508.05049) | \ | Lightweight version for mobile/edge devices. |
| **GMMamba** | ICCV 2025 | [Link](https://openaccess.thecvf.com/content/ICCV2025/html/Zheng_GMMamba_Group_Masking_Mamba_for_Whole_Slide_Image_Classification_ICCV_2025_paper.html) | [Link](https://github.com/titizheng/GMMamba) | WSI analysis with position-aware mechanisms. |
| **XFMamba** | MICCAI 2025 | [Link](https://papers.miccai.org/miccai-2025/1023-Paper1773.html) | [Link](https://github.com/XZheng0427/XFMamba) | Multi-view fusion for X-ray/MRI. |
| **nnMamba** | IEEE-ISBI 2025 | [Link](https://ieeexplore.ieee.org/abstract/document/10980694) | [Link](https://github.com/lhaof/nnMamba) | Integration of Mamba into the nnU-Net framework. |
| **DermaMamba** | Bioengineering 2025 | [Link](https://www.mdpi.com/2306-5354/12/10/1030) | [Link](https://github.com/hnkhai25/DermoMamba) | Dual-Branch Design combining the CNN and Mamba. |

<a name="detection"></a>
## 3. Detection
*Focus: Lesion detection, anomaly detection, cell detection.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **MambaAD** | NeurIPS 2024 | [Link](https://lewandofskee.github.io/projects/MambaAD/) | [Link](https://github.com/lewandofskee/MambaAD) | Unsupervised anomaly detection (Global + Local). |
| **MambaMIL** | MICCAI 2024 | [Link](https://arxiv.org/abs/2403.06800) | [Link](https://github.com/isyangshu/MambaMIL) | Effectively model long sequences and reduce computational complexity. |
| **SP-Mamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2404.02063) | [Link](https://github.com/JusperLee/SPMamba) | Self-supervised anomaly detection. |
| **SpectMamba** | arXiv 2025 | [Link](https://arxiv.org/abs/2509.01080) | [Link](https://github.com/Tinkle01/SpectMamba) | Uses frequency domain learning for small target detection. |
| **CellMamba** | arXiv 2025 | [Link](https://github.com/ChengAoShen/CellMamba) | [Link](https://arxiv.org/abs/2512.21803) | Dense cell detection in pathology images. |


<a name="reconstruction--enhancement"></a>
## 4. Reconstruction & Enhancement
*Focus: MRI acceleration, Low-dose CT denoising, Super-resolution.* 

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **DenoMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2409.13094) | [Link](https://github.com/icon-lab/DenoMamba?tab=readme-ov-file) | Image denoising framework. |
| **MambaMIR** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.18451) | \ | Dynamic weights and linear complexity. |
| **FD-Vision Mamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2402.06378) | [Link](https://github.com/zzr-idam/FDV-NET) | Linear complexity, global receptive field. |
| **MambaRecon** | WACV 2025 | [Link](https://openaccess.thecvf.com/content/WACV2025/html/Korkmaz_MambaRecon_MRI_Reconstruction_with_Structured_State_Space_Models_WACV_2025_paper.html) | [Link](https://github.com/yilmazkorkmaz1/MambaRecon?tab=readme-ov-file) | MRI reconstruction with linear complexity (O(N)). |
| **CT-Mamba** | CMIG 2025 | [Link](https://www.sciencedirect.com/science/article/abs/pii/S0895611125001041?via%3Dihub) | [Link](https://github.com/linxuan-li/CT-Mamba?tab=readme-ov-file) | Low-dose CT denoising. |
| **MMR-Mamba** | MIA 2025 | [Link](https://www.sciencedirect.com/science/article/abs/pii/S1361841525000969) | [Link](https://github.com/zoujing925/MMR-Mamba?tab=readme-ov-file) | Multi-modal MRI reconstruction. |
| **UltrasOM** | CMPB 2025 | [Link](https://www.sciencedirect.com/science/article/abs/pii/S0169260725002603?via%3Dihub) | \ | Ultrasound video analysis & motion estimation. |
| **UltrasODM** | AAAI 2026 | [Link](https://arxiv.org/abs/2512.07756) | [Link](https://github.com/AnandMayank/UltrasODM) | Real-time detection of scanning errors and guidance for doctors to make corrections. |

<a name="registration"></a>
## 5. Registration
*Focus: Deformable registration, multi-modal alignment.*

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **RegMamba** | MDPI 2024 | [Link](https://www.mdpi.com/2079-9292/13/16/3305) | [Link](https://github.com/Hexu00/Regmamba) | Hybrid CNN-Mamba for large deformation handling. |
| **VMambaMorph** | arXiv 2024 | [Link](https://arxiv.org/abs/2404.05105) | [Link](https://github.com/ziyangwang007/VMambaMorph) | 3D deformable registration with cross-scan mechanism. |
| **MambaMorph** | arXiv 2024 | [Link](https://arxiv.org/abs/2401.13934) | [Link](https://github.com/Guo-Stone/MambaMorph) | Efficient registration baseline. |
| **MambaNetLK** | arXiv 2025 | [Link](https://arxiv.org/abs/2511.00260) | [Link](https://github.com/mobarakol/MambaNetLK) | Point cloud registration for surgical navigation. |

<a name="generation"></a>
## 6. Generation & Multimodal
*Focus: Image synthesis, Cross-modality generation, Report generation.*

| Model | Publication | Paper | Code | Description |
| :--- | :--- | :--- | :--- | :--- |
| **DiM** | arXiv 2024 | [Link](https://arxiv.org/abs/2405.14224) | [Link](https://github.com/tyshiwo1/DiM-DiffusionMamba) | Efficient high-res generation, replaces Attention in U-Net. |
| **I2I-Mamba** | arXiv 2024 | [Link](https://arxiv.org/html/2405.14022v4) | [Link](https://github.com/icon-lab/I2I-Mamba) | Image-to-Image translation (e.g., MRI to CT). |
| **VM-DDPM** | arXiv 2024 | [Link](https://arxiv.org/abs/2405.05667) | \ | Balance structural texture consistency and maintain linear computational complexity. |
| **MambaDFuse** | arXiv 2024 | [Link](https://arxiv.org/abs/2404.08406) | [Link](https://github.com/Lizhe1228/MambaDFuse) | State-of-the-art (SOTA) image fusion performance, outperforming CNN and Transformer. |
| **ClinicalMamba** | arXiv 2024 | [Link](https://arxiv.org/abs/2403.05795) | [Link](https://github.com/whaleloops/ClinicalMamba) | A Generative Clinical Language Model on Longitudinal Clinical Notes. |
| **FusionMamba** | arXiv 2025 | [Link](https://arxiv.org/abs/2404.09498) | [Link](https://github.com/millieXie/FusionMamba) | Dynamic Feature Enhancement for Multimodal Image Fusion with Mamba. |
| **MD-Dose** | IEEE-BIBM 2024 | [Link](https://ieeexplore.ieee.org/abstract/document/10822581) | [Link](https://github.com/LinjieFu-U/mamba_dose) | Superior to existing methods, this method can locate the dose region of OARs. |
| **RRG-Mamba** | IJCAI 2025 | [Link](https://www.ijcai.org/proceedings/2025/824) | [Link](https://github.com/Eleanorhxd/RRG-Mamba) | Radiology report generation. |
| **R2Gen-Mamba** | IEEE-ISBI 2025 | [Link](https://ieeexplore.ieee.org/document/10980814) | [Link](https://github.com/YonghengSun1997/R2Gen-Mamba) | Radiology report generation. |

<a name="reviews"></a>
## Review Papers
### 1) General Mamba & SSM Surveys 
*Focus: Broad reviews of State Space Models, Mamba architectures, and Computer Vision applications.*

| Title | Venue | Date | Paper | Code | Key Focus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **State Space Models Survey** | arXiv | 2024.01 | [Link](https://arxiv.org/abs/2401.13739) | [Link](https://github.com/MzeroMiko/State-Space-Model-Survey) | Early comprehensive review of SSMs as an alternative to Transformers. |
| **Visual Mamba Survey** | arXiv | 2024.04 | [Link](https://arxiv.org/abs/2404.18861) | [Link](https://github.com/lx666666/Vision-Mamba-Survey) | Review of Mamba specifically for Computer Vision tasks (Image/Video). |
| **Vision Mamba Taxonomy** | arXiv | 2024.05 | [Link](https://arxiv.org/abs/2405.04404) | [Link](https://github.com/Baidu/Vision-Mamba-Survey) | Detailed taxonomy of Mamba models in vision (Backbones & Applications). |
| **SSM Sequence Survey** | arXiv | 2024.06 | [Link](https://arxiv.org/abs/2406.09062) | \ | Survey on recurrence and state-space modeling in the Transformer era. |
| **A Survey of Mamba** | arXiv | 2024.08 | [Link](https://arxiv.org/abs/2408.01129) | \ | General survey covering architectures, efficient training, and hardware. |
| **Mamba Architecture Survey**| arXiv | 2025.02 | [Link](https://arxiv.org/abs/2502.07161) | \ | Recent survey focusing on architectural advancements like bidirectional scanning. |
| **From S4 to Mamba** | arXiv | 2025.03 | [Link](https://arxiv.org/abs/2503.18970) | \ | Traces the evolution from S4 to Mamba, S5, and Jamba. |

### 2) Surveys in Medical Imaging 
*Focus: Specific reviews of Mamba applied to medical image analysis.*

| Title | Venue | Date | Paper | Code | Key Focus |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Survey of Mamba (Medical)**| arXiv | 2024.06 | [Link](https://arxiv.org/abs/2406.02642) | \ | The first comprehensive survey dedicated to medical Mamba architectures. |
| **Mamba-in-Medical-Imaging** | arXiv | 2024.10 | [Link](https://arxiv.org/abs/2410.02362) | [Link](https://github.com/1500355469/Mamba-in-Medical-Imaging) | A systematic review of papers, code, and datasets in medical imaging. |


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
