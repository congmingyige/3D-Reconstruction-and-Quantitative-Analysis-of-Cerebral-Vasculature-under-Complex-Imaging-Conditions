# 中文版本
## 目录
- [使用指南](#使用指南)
- [PPT下载链接](#ppt下载链接)
- [欢迎交流](#欢迎学术上的任何交流特别是关于医学图像处理脑血管分割网络分析血流模拟的内容通过邮箱1249591860qqcom或者github-issues联系我即可)
- [关于本工作](#关于本工作)
- [展示](#展示)
- [工作文字介绍](#工作文字介绍)

## 使用指南
复杂图像条件下脑血管三维重建与定量分析PPT等内容

版本1 陈冠斌_PPT_联影_分子影像事业部算法_二面_20251023：比较全的一个版本

版本2 陈冠斌_复杂图像条件下脑血管三维重建与定量分析_最新的版本_但是有不少待添加的内容_20251023.pptx：最新的版本，相比版本1有不少新内容，也有不少内容是待添加的内容（PPT上标注有红色TBD的所在页）。因为最近比较忙，毕竟在找工作，面试也挺多，所以更新可能会比较慢，如果有快速更新期待和需求的话，请联系我。

本人正积极寻求合适的工作机会，若您有相关岗位推荐或招聘需求，欢迎通过邮箱1249591860@qq.com与我联系，期待与您沟通！

## PPT下载链接
阿里云盘：https://www.alipan.com/s/PNWLD9AJZvw

夸克云盘：https://pan.quark.cn/s/c100a99df184

百度网盘：https://pan.baidu.com/s/1hp6YO0RXzVHWLTN_Nlm_tw?pwd=0000

OneDrive：https://1drv.ms/f/c/e7e1e12530973d68/EvIgfE5cHpZJgYIsUf_wfCUBv2X4y9yyyDSMXGPrOSh57w?e=5uJcAc

## 欢迎学术上的任何交流，特别是关于医学图像处理、脑血管、分割、网络分析、血流模拟的内容，通过邮箱1249591860@qq.com或者GitHub Issues联系我即可

## 关于本工作
庄茁院士（王鹏老师）和骆清铭院士、龚辉教授团队（李安安、李宇昕老师）合作课题

**庞大数据集**：全脑完整精细血管 x 24；健康 / 损伤数据

离体数据（**离体的缺陷掩盖不了它的全脑完整高分辨率金子般的价值**）

**所有**脑血管、**任何位置**都能清晰可见，**高清无码**，**血管科研人员**需要它，**临床人员**需要它（**CT、MRI无法到达的分辨率**），还有一些**药物研发**、**疾病模型**、**血流模拟**的工作需要它

**毛细血管分辨率** 0.35 x 0.35 x 1 μm

标记 / 生物试验：FITC / Dylight；血管灌注 / 转基因

单个数据图像大小：11400 x 8000 x 13200

**庞大的单套数据大小规模和血管数据（10+，100+，1000+套数据），它来了分割精度要求的巨大挑战，人工标记血管和修改分割后错误位置无异于痴人说梦。无论是有监督方法还是无监督方法，哪怕提升一点，对于之后的定量分析、网络分析和血流模拟，都是巨大的提升**

灰度值：8bit，0 - 255

预处理 + 配准

有监督方法：
- 方法：**Swin Transformer + 5个解决分割断裂/去噪的模块；Accuracy、F1、Dice、HD95参数效果最优**
- 数据集：600 / 400个160 x 160 x 160大小的1 x 1 x 1 μm的数据块。大致按照训练集 / 测试集 / 验证集 8 : 1 : 1的比例
- 训练：A100 * 1
- 推理：RTX 5000 * 15，同时并行跑多套数据和多个任务，附带健壮性脚本


无监督方法： vesselFM（**也是很强烈推荐他组的这个工作**）

## 展示
<img width="1791" height="797" alt="image" src="https://github.com/user-attachments/assets/e5fa9efc-31ea-46cf-b761-1f2f0adeec4a" />

<br> <br> <img width="909" height="369" alt="image" src="https://github.com/user-attachments/assets/10098c93-8993-4e43-b1be-86760b96dd44" />

<br> <br> <img width="539" height="67" alt="image" src="https://github.com/user-attachments/assets/dada5612-7e7c-4fa2-af7f-080e06a18dd9" />

<br> <br> <img width="4400" height="2971" alt="该研究工作流程图" src="https://github.com/user-attachments/assets/e98ff8b6-cd0e-4237-bc3c-d935c94436fb" />

为了解决分割断裂的新增的模块，它带来了新的棋盘格伪影的问题
<br> <br> <img width="1214" height="1461" alt="image" src="https://github.com/user-attachments/assets/be1821c8-8745-4658-b6d3-85e8126c18a0" />

<br> <br> <img width="1422" height="812" alt="image" src="https://github.com/user-attachments/assets/64990791-682c-4639-b667-646ce20f2252" />

<br> <br> <img width="2754" height="983" alt="image" src="https://github.com/user-attachments/assets/a58a9fed-1d82-44ee-83b1-309c1b52234a" />

<br> <br> <img width="2712" height="970" alt="image" src="https://github.com/user-attachments/assets/6b95bca2-531d-440d-9593-3984f97d80b1" />

<br> <br> <img width="2087" height="1368" alt="image" src="https://github.com/user-attachments/assets/d1f54d7c-f6ea-40bd-9783-e79460960f44" />

<br> <img width="2738" height="1195" alt="image" src="https://github.com/user-attachments/assets/cc3b93a9-3ae0-45e6-aeab-899520f01288" />

业界做血流模拟的工作
<br> <br> <img width="1958" height="1406" alt="image" src="https://github.com/user-attachments/assets/c8608447-95a2-4862-b4b6-6285d1800c91" />

## 工作文字介绍（版本1）
# 基于Swin Transformer方法的脑损伤全脑高分辨率血管的分割、骨架化和网络分析（已开源，见GitHub）

**时间：** 2024.6 - 2025.7

**项目链接：** [https://github.com/congmingyige/3D-Reconstruction-and-Quantitative-Analysis-of-Cerebral-Vasculature-under-Complex-Imaging-Conditions](https://github.com/congmingyige/3D-Reconstruction-and-Quantitative-Analysis-of-Cerebral-Vasculature-under-Complex-Imaging-Conditions)

---

### 1. 🔬 项目背景与描述

* **生物学背景**：脑很脆弱，短暂的大脑缺血带来脑损伤，脑血管系统是亟待研究的核心需求。脑血管网络就像一个城市的交通系统，动脉网络负责把最新鲜的“外卖”（富含氧气和葡萄糖的血液）送往脑四处，“送货上门”的毛细血管网络密集到每一个脑细胞旁边都有，脑细胞吃完“外卖”，会扔出“垃圾”（二氧化碳和废物），这些垃圾被扔回血液，通过静脉网络回收。
* **问题和描述**：脑血管的结构类似于地下庞大的水管网络，弯曲波折。成像数据需要精细，微血管的损伤在TBI的影响中发挥了重要作用。成像数据需要完整，因为脑血管是一个庞大的体系，需要系统性的研究。当满足了所有脑血管、任何位置都能清晰可见，高清，血管科研人员需要它，临床人员需要它（CT、MRI无法到达的分辨率），还有一些药物研发、疾病模型、血流模拟的工作需要它。离体数据的缺陷掩盖不了它的全脑完整高分辨率金子般的价值。我们需要对这些脑血管数据进行**分割、骨架化和网络分析**。
* **任务分工**：庄茁院士和骆清铭院士、龚辉教授团队合作课题。前者负责物理损伤实验，它是数千万军工项目的一部分，后者负责标记/转基因、生物、成像实验，它具有成像优势，曾发表在Science，可以获得离体全脑高分辨率血管数据，极少数单位能完成此工作。**我负责后续的图像处理工作，包括预处理、分割、骨架化和网络分析。**

---

### 2. 挑战与痛点

* **图像分割数据规模**：单个数据图像大小为 $11400 \times 8000 \times 13200$。全脑完整精细血管 $\times 24$；包括健康 / 损伤数据。
* **图像数据规模庞大带来的痛点问题**：庞大的单套数据大小规模和血管数据（$10^1$、$10^2$、$10^3$、$10^4$量级），它带来了分割精度要求的巨大挑战，人工标记血管和修改分割后的错误位置无异于痴人说梦。无论是有监督方法分割还是无监督方法分割，哪怕提升一点，对于之后的定量分析、网络分析和血流模拟，都是巨大的提升。
* **图像数据特征带来的痛点问题**：血管存在二维和三维上的边缘断裂，信号不连续，干扰信号等问题。数据为三维数据，数据量极大，而且血管直径跨越多个数量级且结构复杂。

---

### 3. 核心方法与模型改进

* **有监督深度学习分割方法**：共19种模型（不包括效果不好的模型）。有CV领域经典分割算法VoxResNet、FCN、VNet，有专门针对管状结构的顶会工作DSCNet，有常用的医学分割模型U-Net和nnUNet，有专门分割医学细胞、器官的分割模型nnFormer、UNETR++，有SAM作为主要模块的模型，如MedSAM2、SAM2-UNet（2D拼接）。
* **Swin Transformer方法优越性**：
    * 本工作把 **Swin Transformer** 应用到医学领域脑血管分割任务中。
    * 它采用**层级特征**，解决“单尺度”问题；血管直径 $5\mu m - 500\mu m$；适用于多尺度信息的密集分割任务。
    * 它采用**高效的计算**，解决“计算量爆炸”问题；它采用**窗口注意力**，计算复杂度从平方级 $O(N \times N)$ 降至线性级 $O(N \times 49)$；它利于处理大图像，血管边缘分割效果较好。
    * 它采用**滑动窗口**，W-MSA和SW-MSA，来增大感受野，大的感受野能更好理解损伤的情况。
* **Swin Transformer分割遇到的问题和模型改进**：
    * Swin Transformer 出现同一血管被分割成多个血管（血管断裂）的问题。
    * **改进方法**：采用了 **SENet** 保证血管分割的完整性；采用 $5 \times 1 \times 1$ 的卷积增加 Z 方向的连通性；采用 $3 \times 3 \times 3$ 卷积叠加去增加小范围连通性。
    * **去噪与去伪影**：采用了小型学习网络进行去噪，并构建了一个复杂的**棋盘格伪影去除模型**。最后进行了消融实验来验证增加模块的有效性。
* **零样本分割方法**：
    * **背景**：标注过程高度依赖专家知识、耗时费力，不同批次数据可迁移性不足。
    * **研究工作**：研究了零样本学习方法 **SAM2、SAMURAI、vesselFM** 等，并进行了改造和效果评估。vesselFM效果显著，但仍需在伪影和血管分叉处进行优化。

---

### 4. 运行环境与成果评估

* **运行环境**：网络使用 **Pytorch** 实现。
    * **训练**：配备 4 个 NVIDIA A100 GPU 80GB 的服务器上并行训练。
    * **推理**：配备 15 个 NVIDIA RTX 5000 32GB 的服务器上进行推理。
* **全流程 Pipeline**：采用脚本执行全脑血管分割、分析全流程 Pipeline，并进行监控和管理，包括分割任务中块的多线程分配，一键在所有服务器节点上执行任务，自动检查所有程序运行状态。
* **生产效率**：构建了血管“工厂”，**15台GPU服务器每2天能“生产”15套数据**（分割、骨架化和分析）。
* **评估指标**：采用 Accuracy、Precision、Recall、F1 Score、Dice、clDice、HD、HD95 等参数进行评估。
* **核心成果**：本研究方法在 Accuracy、F1 Score、Dice、HD95 取得最好效果，在重要的 **Dice 指标上，比其它所有方法优 $1-2\%$ 以上**。
* **实现24套数据全脑分割和应用**：分别从长度密度、分叉点密度、血管夹角、子图结构和环结构等多个维度进行分析，结果显示损伤组和对照组在多个参数上具有显著性差异。按照脑区划分，有两种血管损伤模式，包括**局部损伤和整体稀疏**。



## 工作文字介绍（版本2）
### [基于Swin Transformer方法的脑损伤全脑高分辨率血管的分割、骨架化和网络分析](https://github.com/congmingyige/3D-Reconstruction-and-Quantitative-Analysis-of-Cerebral-Vasculature-under-Complex-Imaging-Conditions)（已开源，见GitHub）  
*2024.6-2025.7*

- **生物学背景**：脑具有脆弱性，短暂缺血会导致脑损伤，脑血管系统是核心研究对象。脑血管网络类似城市交通系统：动脉网络输送含氧气和葡萄糖的血液（"外卖"）至全脑，毛细血管密集分布于每个脑细胞旁，静脉网络回收代谢废物（"垃圾"）。

- **问题和描述**：脑血管结构类似地下复杂水管网络，弯曲且分支多。研究需高精度（微血管损伤在TBI中作用关键）和完整性（全脑系统研究）的成像数据，其分辨率超越CT、MRI，可支撑科研、临床、药物研发、疾病模型及血流模拟。离体数据虽有局限，但全脑完整高分辨率特性极具价值，需对其进行分割、骨架化和网络分析。

- **任务分工**：庄茁院士团队（负责物理损伤实验，属千万级军工项目）与骆清铭院士、龚辉教授团队（负责标记/转基因、生物及成像实验，具成像优势，成果曾发表于*Science*，可获取离体全脑高分辨率血管数据，少数单位能完成）合作课题。本人负责后续图像处理，包括预处理、分割、骨架化和网络分析。

- **图像分割数据规模**：单数据图像尺寸为$11400 \times 8000 \times 13200$，含24套全脑完整精细血管数据（含健康/损伤样本）。

- **数据规模带来的痛点**：单套数据量大，血管数量达$10^1$至$10^4$量级，导致分割精度挑战极大，人工标记和修正错误几乎不可能。无论有监督或无监督方法，分割精度的微小提升都对后续定量分析、网络分析和血流模拟意义重大。

- **数据特征带来的痛点**：血管存在二维/三维边缘断裂、信号不连续、干扰信号等问题；数据为三维且量大，血管直径跨多个数量级，结构复杂。

- **有监督深度学习分割方法**：测试19种模型（不含效果差的模型），包括CV经典算法（VoxResNet、FCN、VNet）、管状结构专用顶会工作（DSCNet）、医学分割常用模型（U-Net、nnUNet）、医学细胞/器官分割模型（nnFormer、UNETR++）及基于SAM的模型（MedSAM2、SAM2-UNet（2D拼接））。

- **Swin Transformer方法优越性**：将其应用于脑血管分割，优势在于：
  - 层级特征解决"单尺度"问题，适配直径$5\mu m - 500\mu m$的多尺度血管，适用于密集分割任务；
  - 高效计算解决"计算量爆炸"问题，窗口注意力将计算复杂度从$O(N \times N)$降至$O(N \times 49)$，利于处理大图像，可获取有效非冗余区域信息，血管边缘分割效果佳；
  - 滑动窗口（W-MSA和SW-MSA）增大感受野，更易理解损伤情况（小感受野易"管中窥豹"）。

- **Swin Transformer分割的改进**：
  - 解决血管断裂问题：采用SENet自动学习重要特征通道以保证完整性，通过$5 \times 1 \times 1$卷积增强Z方向连通性，$3 \times 3 \times 3$卷积叠加提升小范围连通性；
  - 解决噪点和棋盘格伪影：用小型学习网络去噪，构建复杂模型去除伪影；
  - 通过消融实验验证新增模块的有效性。

- **零样本分割方法**：针对标注依赖专家知识、耗时费力、存在"观察者间误差"及有监督学习迁移性不足等问题，研究并改造零样本学习方法（SAM2、SAMURAI、vesselFM）。其中vesselFM效果显著，但在伪影和血管分叉处表现欠佳。

- **运行环境**：基于Pytorch实现，在4卡NVIDIA A100（80GB）服务器上并行训练，15台NVIDIA RTX 5000（32GB）服务器上推理。通过脚本实现全流程Pipeline（分割、骨架化、分析）的监控与管理，包括多线程分配任务块、多节点一键执行、自动检查运行状态。构建血管"工厂"，15台GPU服务器每2天可"生产"15套数据（完成分割、骨架化和分析）。

- **评估指标**：采用Accuracy、Precision、Recall、F1 Score、Dice、clDice、HD、HD95等评估。本方法在Accuracy、F1 Score、Dice、HD95指标上最优，其中关键指标Dice较其他方法高1-2%以上。

- **24套数据全脑分割及应用**：从长度密度、分叉点密度、血管夹角、子图结构和环结构等维度分析，发现损伤组与对照组在多个参数上有显著差异。按脑区划分，存在局部损伤和整体稀疏两种血管损伤模式。

---
---





# English Version
## Table of Contents
- [Usage Guide](#usage-guide)
- [PPT Download Links](#ppt-download-links)
- [Academic Discussion Welcome](#feel-free-to-contact-me-for-any-academic-discussion-especially-regarding-medical-image-processing-cerebral-vasculature-segmentation-network-analysis-or-blood-flow-simulation-via-email-at-1249591860qqcom-or-github-issues)
- [About This Work](#about-this-work)
- [Showcase](#showcase)

---

## Usage Guide
3D Reconstruction and Quantitative Analysis of Cerebral Vasculature under Complex Imaging Conditions - PPT and other content.

Version 1 Chen Guanbin_PPT_United Imaging_Molecular Imaging Algorithm Dept_Second Interview_20251023: A relatively complete version.

Version 2 Chen Guanbin_3D Reconstruction and Quantitative Analysis..._Latest Version_but many contents to be added_20251023.pptx: The latest version, which contains significant new content compared to Version 1, but also has many parts yet to be added (marked with red "TBD" on the corresponding slides). I am currently busy with job searching and interviews, so updates may be slow. If you have an urgent need for updates, please contact me.

I am actively seeking suitable job opportunities. If you have any relevant positions or recruitment needs, please feel free to contact me at 1249591860@qq.com. I look forward to hearing from you!

## PPT Download Links
Aliyun Drive: https://www.alipan.com/s/PNWLD9AJZvw

Quark Drive: https://pan.quark.cn/s/c100a99df184

Baidu Netdisk: https://pan.baidu.com/s/1hp6YO0RXzVHWLTN_Nlm_tw?pwd=0000

OneDrive：https://1drv.ms/f/c/e7e1e12530973d68/EvIgfE5cHpZJgYIsUf_wfCUBv2X4y9yyyDSMXGPrOSh57w?e=5uJcAc

## Feel free to contact me for any academic discussion, especially regarding medical image processing, cerebral vasculature, segmentation, network analysis, or blood flow simulation, via email at 1249591860@qq.com or GitHub Issues.

## About This Work
A collaborative project with Academician Zhuang Zhuo (Teacher Wang Peng) and the team of Academician Luo Qingming and Professor Gong Hui.

**Massive Dataset**: Whole-brain fine vasculature x 24; healthy / injury data.

Ex-vivo data (**The limitations of ex-vivo data do not diminish the golden value of its whole-brain, high-resolution integrity**).

**All** cerebral vessels, at **any location**, are clearly visible, **high-definition**, needed by **vascular researchers** and **clinicians** (**at a resolution unattainable by CT/MRI**), as well as for **drug development**, **disease modeling**, and **blood flow simulation**.

**Capillary resolution** 0.35 x 0.35 x 1 μm

Labeling / Bio-experiments: FITC / Dylight; Vascular Perfusion / Transgenic

Single data image size: 11400 x 8000 x 13200

**The massive scale of a single dataset and the sheer volume of vascular data (10+, 100+, 1000+ datasets) pose an enormous challenge to segmentation accuracy. Manually labeling vessels or correcting segmentation errors is an impossible task. Whether using supervised or unsupervised methods, even a slight improvement is a huge boost for subsequent quantitative analysis, network analysis, and blood flow simulation.**

Grayscale value: 8bit, 0 - 255

Preprocessing + Registration

Supervised Method:
  - Method: **Swin Transformer + 5 modules to address segmentation fractures/denoising; optimal results on Accuracy, F1, Dice, HD95 metrics**
  - Dataset: 600 / 400 data blocks of size 160 x 160 x 160 at 1 x 1 x 1 μm. Roughly an 8:1:1 ratio for training / testing / validation.
  - Training: A100 * 1
  - Inference: RTX 5000 * 15, running multiple datasets and tasks in parallel, with robust scripts.
 
Unsupervised Method: vesselFM (**I also highly recommend their group's work on this**)

## Showcase
<img width="1791" height="797" alt="image" src="https://github.com/user-attachments/assets/e5fa9efc-31ea-46cf-b761-1f2f0adeec4a" />

<br> <br> <img width="909" height="369" alt="image" src="https://github.com/user-attachments/assets/10098c93-8993-4e43-b1be-86760b96dd44" />

<br> <br> <img width="539" height="67" alt="image" src="https://github.com/user-attachments/assets/dada5612-7e7c-4fa2-af7f-080e06a18dd9" />

<br> <br> <img width="4400" height="2971" alt="Workflow diagram of this research" src="https://github.com/user-attachments/assets/e98ff8b6-cd0e-4237-bc3c-d935c94436fb" />

The new modules added to solve segmentation fractures introduced a new problem of checkerboard artifacts.
<br> <br> <img width="1214" height="1461" alt="image" src="https://github.com/user-attachments/assets/be1821c8-8745-4658-b6d3-85e8126c18a0" />

<br> <br> <img width="1422" height="812" alt="image" src="https://github.com/user-attachments/assets/64990791-682c-4639-b667-646ce20f2252" />

<br> <br> <img width="2754" height="983" alt="image" src="https://github.com/user-attachments/assets/a58a9fed-1d82-44ee-83b1-309c1b52234a" />

<br> <br> <img width="2712" height="970" alt="image" src="https://github.com/user-attachments/assets/6b95bca2-531d-440d-9593-3984f97d80b1" />

<br> <br> <img width="2087" height="1368" alt="image" src="https://github.com/user-attachments/assets/d1f54d7c-f6ea-40bd-9783-e79460960f44" />

<br> <img width="2738" height="1195" alt="image" src="https://github.com/user-attachments/assets/cc3b93a9-3ae0-45e6-aeab-899520f01288" />

Blood flow simulation work in the industry
<br> <br> <img width="1958" height="1406" alt="image" src="https://github.com/user-attachments/assets/c8608447-95a2-4862-b4b6-6285d1800c91" />

## Work Introduction (Version 1)

```markdown
## 工作文字介绍（版本1）
# Segmentation, Skeletonization, and Network Analysis of High-Resolution Whole-Brain Vasculature with Brain Injury using Swin Transformer Method (Open Source, See GitHub)

**Time:** 2024.6 - 2025.7

**Project Link:** [https://github.com/congmingyige/3D-Reconstruction-and-Quantitative-Analysis-of-Cerebral-Vasculature-under-Complex-Imaging-Conditions](https://github.com/congmingyige/3D-Reconstruction-and-Quantitative-Analysis-of-Cerebral-Vasculature-under-Complex-Imaging-Conditions)

---

### 1. 🔬 Project Background and Description

* **Biological Background**: The brain is fragile, and transient cerebral ischemia leads to brain injury, making the cerebrovascular system a core area of urgent research. The cerebrovascular network is like a city's transportation system: the arterial network is responsible for delivering the freshest "takeaway" (blood rich in oxygen and glucose) throughout the brain; the capillary network, which provides "door-to-door delivery," is dense next to every brain cell; after consuming the "takeaway," brain cells discard "waste" (carbon dioxide and waste products), which is returned to the blood and recycled through the venous network.
* **Problem and Description**: The structure of cerebral vasculature resembles a massive, winding underground pipe network. Imaging data needs to be fine-grained, as microvascular damage plays a crucial role in the effects of TBI. Imaging data needs to be complete, as the cerebrovascular system is a vast network requiring systematic study. When all blood vessels, at any location, are clearly visible and high-definition, it is needed by vascular researchers, clinicians (at a resolution unattainable by CT/MRI), and for work in drug development, disease modeling, and blood flow simulation. The limitations of *ex vivo* data cannot obscure its golden value of whole-brain complete high resolution. We need to perform **segmentation, skeletonization, and network analysis** on these cerebrovascular data.
* **Task Division**: A collaborative project with Academician Zhuang Zhuo, Academician Luo Qingming, and Professor Gong Hui's team. The former is responsible for the physical injury experiments, which are part of a multi-million dollar military project. The latter is responsible for labeling/transgenesis, biology, and imaging experiments, possessing imaging advantages and having published in *Science*, capable of obtaining *ex vivo* whole-brain high-resolution vascular data, a feat accomplished by very few institutions. **I am responsible for the subsequent image processing work, including pre-processing, segmentation, skeletonization, and network analysis.**

---

### 2. Challenges and Pain Points

* **Image Segmentation Data Scale**: The size of a single data image is $11400 \times 8000 \times 13200$. Whole-brain complete fine vasculature $\times 24$ sets; including healthy / injured data.
* **Pain Points Caused by Massive Data Scale**: The massive size of single-set data and the scale of vascular data ($10^1$, $10^2$, $10^3$, $10^4$ magnitudes) bring a huge challenge to the required segmentation accuracy. Manually labeling vessels and correcting segmentation errors is virtually impossible. Even a slight improvement, whether in supervised or unsupervised segmentation methods, is a huge boost for subsequent quantitative analysis, network analysis, and blood flow simulation.
* **Pain Points Caused by Image Data Characteristics**: Vessels have 2D and 3D edge breaks, signal discontinuity, and interference signals. The data is 3D, extremely large in volume, and vessel diameters span multiple orders of magnitude with complex structures.

---

### 3. Core Methods and Model Improvements

* **Supervised Deep Learning Segmentation Methods**: A total of 19 models were tested (excluding models with poor results). This includes classic CV segmentation algorithms VoxResNet, FCN, VNet; DSCNet, a top-tier paper work specifically for tubular structures; common medical segmentation models U-Net and nnUNet; models specialized for medical cell/organ segmentation nnFormer, UNETR++; and models using SAM as the main module, such as MedSAM2, SAM2-UNet (2D stitching).
* **Swin Transformer Method Superiority**:
    * This work applies the **Swin Transformer** to the cerebrovascular segmentation task in the medical field.
    * It uses **hierarchical features** to solve the "single-scale" problem; vessel diameters $5\mu m - 500\mu m$; suitable for dense segmentation tasks with multi-scale information.
    * It uses **efficient computation** to solve the "computational explosion" problem; it uses **Window Attention**, reducing computational complexity from quadratic $O(N \times N)$ to linear $O(N \times 49)$; it is beneficial for processing large images, yields better segmentation results for vessel edges, and allows obtaining more effective non-redundant regional information from large images.
    * It uses **sliding windows**, W-MSA and SW-MSA, to increase the receptive field; a large receptive field allows for a better understanding of the injury situation, whereas a small receptive field is somewhat like looking at a leopard through a tube.
* **Swin Transformer Segmentation Issues and Model Improvements**:
    * Swin Transformer shows good segmentation results in most areas, but it exhibits the problem of a single vessel being segmented into multiple segments (vessel discontinuity).
    * **Improvement Methods**: This work adopted **SENet** to automatically learn which feature channels are more important, ensuring the integrity of vessel segmentation; used $5 \times 1 \times 1$ convolution to increase Z-direction connectivity; and used $3 \times 3 \times 3$ convolution stacking to increase small-range connectivity, resolving the vessel discontinuity issue.
    * **Denoising and Artifact Removal**: Swin Transformer segmentation also contained some noise, and the added modules introduced checkerboard artifacts. This work employed a small learning network for denoising and constructed a complex checkerboard artifact removal model. Finally, ablation experiments were conducted to verify the effectiveness of the added modules.
* **Zero-Shot Segmentation Methods**:
    * **Background**: The annotation process is highly dependent on expert knowledge, time-consuming and laborious, with significant time and economic costs. Subjective judgments, experience levels, and operational standards vary among annotators, inevitably leading to significant "inter-observer error." Furthermore, data characteristics often differ across batches, resulting in poor transferability of supervised learning. Foundation model methods are used to solve these problems; after large-scale training, these models can be fine-tuned using zero-shot, few-shot, and other methods when encountering new data features, quickly achieving relatively ideal results.
    * **Research Work**: This work investigated and adapted zero-shot learning methods such as **SAM2, SAMURAI, and vesselFM**, and conducted effectiveness evaluations. vesselFM showed significant results, but segmentation was not perfectly ideal at artifacts and vessel bifurcations.

---

### 4. Runtime Environment and Results Evaluation

* **Runtime Environment**: The network is implemented using **Pytorch**.
    * **Training**: Parallel training was conducted on a server equipped with 4 NVIDIA A100 GPUs 80GB.
    * **Inference**: Inference was performed on 15 servers equipped with NVIDIA RTX 5000 32GB.
* **Full-Process Pipeline**: A script was used to execute the full-process Pipeline for whole-brain vessel segmentation and analysis, including monitoring and management, such as multi-threaded block allocation in the segmentation task, one-click execution on all server nodes, and automatic checking of all program running states. A vascular "factory" was built, allowing 15 GPU servers to "**produce**" (segment, skeletonize, and analyze) 15 sets of data every 2 days.
* **Evaluation Metrics**: Accuracy, Precision, Recall, F1 Score, Dice, clDice, HD, HD95 were used for evaluation.
* **Core Results**: This research method achieved the best results in Accuracy, F1 Score, Dice, and HD95. On the critical **Dice metric, it outperformed all other methods by $1-2\%$ or more**.
* **Implementation of Whole-Brain Segmentation and Application for 24 Datasets**: Analysis was performed from multiple dimensions, including length density, bifurcation point density, vessel angle, subgraph structure, and loop structure. The results show significant differences between the injured group and the control group across multiple parameters. Based on brain region division, two types of vascular injury patterns were identified: **local damage and overall sparsity**.
```

-----

## Work Introduction (Version 2)

```markdown
## 工作文字介绍（版本2）
### [Segmentation, Skeletonization, and Network Analysis of High-Resolution Whole-Brain Vasculature with Brain Injury using Swin Transformer Method](https://github.com/congmingyige/3D-Reconstruction-and-Quantitative-Analysis-of-Cerebral-Vasculature-under-Complex-Imaging-Conditions) (Open Source, See GitHub)  
*2024.6-2025.7*

- **Biological Background**: The brain is fragile, and transient ischemia leads to brain injury, making the cerebrovascular system a core research object. The cerebrovascular network is similar to a city's transportation system: the arterial network transports blood containing oxygen and glucose ("takeaway") throughout the brain, the capillary network is densely distributed next to every brain cell, and the venous network recycles metabolic waste ("trash").

- **Problem and Description**: The cerebral vascular structure resembles a complex underground pipe network, winding and highly branched. Research requires high-precision (microvascular damage is key in TBI) and complete (whole-brain systematic study) imaging data, with resolution surpassing CT/MRI, to support research, clinical work, drug development, disease modeling, and blood flow simulation. Despite limitations, the whole-brain complete high-resolution characteristic of *ex vivo* data is extremely valuable, and we need to perform segmentation, skeletonization, and network analysis on it.

- **Task Division**: A collaborative project between Academician Zhuang Zhuo's team (responsible for physical injury experiments, part of a multi-million dollar military project) and Academician Luo Qingming, Professor Gong Hui's team (responsible for labeling/transgenesis, biology, and imaging experiments, possessing imaging advantages, published in *Science*, capable of acquiring *ex vivo* whole-brain high-resolution vascular data, which few institutions can achieve). I am responsible for subsequent image processing, including pre-processing, segmentation, skeletonization, and network analysis.

- **Image Segmentation Data Scale**: Single data image size is $11400 \times 8000 \times 13200$, including 24 sets of whole-brain complete fine vasculature data (containing healthy/injured samples).

- **Pain Points from Data Scale**: The volume of a single dataset is massive, and the number of vessels reaches $10^1$ to $10^4$ magnitudes, leading to extreme challenges in segmentation accuracy, making manual labeling and error correction nearly impossible. Whether supervised or unsupervised methods are used, even a slight improvement in segmentation accuracy is profoundly significant for subsequent quantitative analysis, network analysis, and blood flow simulation.

- **Pain Points from Data Characteristics**: Vessels exhibit 2D/3D edge breaks, signal discontinuity, and interference signals; the data is 3D and massive, with vessel diameters spanning multiple orders of magnitude and complex structure.

- **Supervised Deep Learning Segmentation Methods**: 19 models were tested (excluding models with poor results), including classic CV algorithms (VoxResNet, FCN, VNet), top-tier conference work dedicated to tubular structures (DSCNet), common medical segmentation models (U-Net, nnUNet), medical cell/organ segmentation models (nnFormer, UNETR++), and SAM-based models (MedSAM2, SAM2-UNet (2D stitching)).

- **Swin Transformer Method Superiority**: Applied to cerebrovascular segmentation, its advantages include:
  - Hierarchical features resolve the "single-scale" issue, adapting to multi-scale vessels with diameters $5\mu m - 500\mu m$, suitable for dense segmentation tasks;
  - Efficient computation resolves the "computational explosion" problem, with Window Attention reducing computational complexity from $O(N \times N)$ to $O(N \times 49)$, beneficial for processing large images, allowing acquisition of effective non-redundant regional information, and excellent vessel edge segmentation;
  - Sliding Windows (W-MSA and SW-MSA) increase the receptive field, facilitating a better understanding of the injury situation (small receptive fields risk "seeing only a small part").

- **Swin Transformer Segmentation Improvements**:
  - Addressing vessel discontinuity: Employed SENet to automatically learn important feature channels to ensure integrity, used $5 \times 1 \times 1$ convolution to enhance Z-direction connectivity, and $3 \times 3 \times 3$ convolution stacking to boost small-range connectivity;
  - Addressing noise and checkerboard artifacts: Used a small learning network for denoising and constructed a complex model to remove artifacts;
  - Effectiveness of added modules verified through ablation experiments.

- **Zero-Shot Segmentation Methods**: To address annotation dependency on expert knowledge, time/cost constraints, "inter-observer error," and poor transferability of supervised learning, zero-shot learning methods (SAM2, SAMURAI, vesselFM) were researched and adapted. vesselFM showed significant results but performed less ideally at artifacts and vessel bifurcations.

- **Runtime Environment**: Implemented based on Pytorch, with parallel training on a server with 4 NVIDIA A100 (80GB) GPUs, and inference on 15 NVIDIA RTX 5000 (32GB) servers. Scripts were used to implement a full-process Pipeline (segmentation, skeletonization, analysis) for monitoring and management, including multi-threaded allocation of task blocks, one-click execution across multiple nodes, and automatic checking of running program status. A vascular "factory" was established, allowing 15 GPU servers to "**produce**" 15 datasets (completed segmentation, skeletonization, and analysis) every 2 days.

- **Evaluation Metrics**: Accuracy, Precision, Recall, F1 Score, Dice, clDice, HD, HD95 were used for evaluation. This method achieved the best results in Accuracy, F1 Score, Dice, and HD95, with the critical Dice metric exceeding other methods by $1-2\%$ or more.

- **Whole-Brain Segmentation and Application for 24 Datasets**: Analysis from dimensions including length density, bifurcation point density, vessel angle, subgraph structure, and loop structure revealed significant differences in multiple parameters between the injured group and the control group. Based on brain region division, two vascular injury patterns were identified: **local damage and overall sparsity**.
```
