[中文版本](#中文版本)
&nbsp;&nbsp;
[English Version](#English-Version)

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

**庞大数据集**：全脑完整精细血管 X 24；健康 / 损伤数据

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

## 工作文字介绍
* **问题和描述**：脑很脆弱，短暂的大脑缺血带来脑损伤，脑血管系统是亟待研究的核心需求。脑血管网络就像一个城市的交通系统，动脉网络负责把最新鲜的“外卖”（富含氧气和葡萄糖的血液）送往脑四处，“送货上门”的毛细血管网络密集到每一个脑细胞旁边都有，脑细胞吃完“外卖”，会扔出“垃圾”（二氧化碳和废物），这些垃圾被扔回血液，通过静脉网络回收。它的结构类似于地下庞大的水管网络。成像数据需要精细，微血管的损伤在TBI的影响中发挥了重要作用。成像数据需要完整，因为脑血管是一个庞大的体系，需要系统性的研究。当满足了所有脑血管、任何位置都能清晰可见，高清，血管科研人员需要它，临床人员需要它（CT、MRI无法到达的分辨率），还有一些药物研发、疾病模型、血流模拟的工作需要它。离体数据的缺陷掩盖不了它的全脑完整高分辨率金子般的价值。

* **任务分工**：庄茁院士和骆清铭院士、龚辉教授团队合作课题。前者负责物理损伤实验，它是数千万军工项目的一部分，后者负责标记/转基因、生物、成像实验，它具有成像优势，曾发表在Science，可以获得离体全脑高分辨率血管数据，极少数单位能完成此工作。我负责后续的图像处理工作，包括预处理、分割、骨架化和网络分析。

* **图像分割数据规模**：单个数据图像大小为$11400 \times 8000 \times 13200$。全脑完整精细血管$\times 24$；包括健康 / 损伤数据。

* **图像数据规模庞大带来的痛点问题**：庞大的单套数据大小规模和血管数据（$10^1$、$10^2$、$10^3$、$10^4$量级），它带来了分割精度要求的巨大挑战，人工标记血管和修改分割后的错误位置无异于痴人说梦。无论是有监督方法分割还是无监督方法分割，哪怕提升一点，对于之后的定量分析、网络分析和血流模拟，都是巨大的提升。

* **图像数据特征带来的痛点问题**：血管存在二维和三维上的边缘断裂，信号不连续，干扰信号等问题。数据为三维数据，数据量极大，而且血管直径跨越多个数量级且结构复杂。

* **有监督深度学习分割方法**：共19种模型（不包括效果不好的模型）。有CV领域经典分割算法VoxResNet、FCN、VNet，有专门针对管状结构的顶会工作DSCNet，有常用的医学分割模型U-Net和nnUNet，有专门分割医学细胞、器官的分割模型nnFormer、UNETR++，有SAM作为主要模块的模型，如MedSAM2、SAM2-UNet（2D拼接）。

* **Swin Transformer方法优越性**：本工作把Swin Transformer应用到医学领域脑血管分割任务中。它采用层级特征，解决“单尺度”问题；血管直径$5\mu m - 500\mu m$；适用于多尺度信息的密集分割任务。它采用高效的计算，解决“计算量爆炸”问题；它采用窗口注意力，计算复杂度从平方级$O(N \times N)$降至线性级$O(N \times 49)$；它利于处理大图像，血管边缘分割效果较好，大图像可以获取更加有效的非冗余区域信息。它采用滑动窗口，W-MSA和SW-MSA，来增大感受野，大的感受野能更好理解损伤的情况，而小的感受野有点类似于管中窥豹。

* **Swin Transformer分割遇到的问题和模型改进**：Swin Transformer在大部分位置上分割效果较好，但是它出现了同一个血管被分割成多个血管的情况，可以类比为一条线段被断成了几截。本工作采用了SENet，自动学习哪些特征通道更重要，保证了血管分割的完整性，采用$5 \times 1 \times 1$的卷积增加Z方向的连通性，采用$3 \times 3\ \times 3$卷积叠加去增加小范围连通性，通过这些方法去解决血管断裂问题。同时，Swin Transformer分割存在少量噪点，以及添加的模块带来了棋盘格伪影，本工作采用了小型学习网络进行去噪，并且构建了一个复杂的棋盘格伪影去除模型。最后进行了消融实验来验证增加模块的有效性。

* **零样本分割方法**：标注过程高度依赖专家知识，耗时费力，具有显著的时间和经济成本。不同标注者的主观判断、经验水平和操作标准难以统一，不可避免地导致了显著的“观察者间误差”。同时不同批次数据的数据特征也不尽相同，有监督学习可迁移性不足。基础模型方法是为解决这些问题而进行的，这类模型经过模型大训练，之后遇到新的特征的数据，可以进行zero-shot、few-shot等手段，进行微调，就能很快获得较为理想的效果。本工作研究了零样本学习方法SAM2、SAMURAI、vesselFM等，并进行了改造和效果评估。vesselFM效果显著，只是在伪影和血管分叉处分割效果不是特别理想。

* **运行环境**：网络使用 Pytorch 实现。实验在配备 4 个 NVIDIA A100 GPU 80GB 的服务器上并行训练，在15个配备NVIDIA RTX 5000 32GB的服务器上进行推理。采用脚本执行全脑血管分割、分析全流程Pipeline，并进行监控和管理。

* **评估指标**：采用Accuracy、Precision、Recall、F1 Score、Dice、clDice、HD、HD95等参数进行评估。本研究方法在Accuracy、F1 Score、Dice、HD95取得最好效果，在重要的Dice指标上，比其它所有方法优$1-2\%$以上。

* **实现24套数据全脑分割和应用**：分别从长度密度、分叉点密度、血管夹角、子图结构和环结构等多个维度进行分析，结果显示损伤组和对照组在多个参数上具有显著性差异。按照脑区划分，有两种血管损伤模式，包括局部损伤和整体稀疏。

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

**Massive Dataset**: Whole-brain fine vasculature X 24; healthy / injury data.

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

<br> <br> <img widthS="539" height="67" alt="image" src="https://github.com/user-attachments/assets/dada5612-7e7c-4fa2-af7f-080e06a18dd9" />

<br> <br> <img width="4400" height="2971" alt="Workflow diagram of this research" src="https://github.com/user-attachments/assets/e98ff8b6-cd0e-4237-bc3c-d935c94436fb" />

The new modules added to solve segmentation fractures introduced a new problem of checkerboard artifacts.
<br> <br> <img width="1214" height="1461" alt="image" src="https://github.com/user-attachments/assets/be1821c8-8745-4658-b6d3-85e8126c18a0" />

<br> <tbr> <img width="1422" height="812" alt="image" src="https://github.com/user-attachments/assets/64990791-682c-4639-b667-646ce20f2252" />

<br> <br> <img width="2754" height="983" alt="image" src="https://github.com/user-attachments/assets/a58a9fed-1d82-44ee-83b1-309c1b52234a" />

<br> <br> <img width="2712" height="970" alt="image" src="https://github.com/user-attachments/assets/6b95bca2-531d-440d-9593-3984f97d80b1" />

<br> <br> <img width="2087" height="1368" alt="image" src="https://github.com/user-attachments/assets/d1f54d7c-f6ea-40bd-9783-e79460960f44" />

<br> <img width="2738" height="1195" alt="image" src="https://github.com/user-attachments/assets/cc3b93a9-3ae0-45e6-aeab-899520f01288" />

Blood flow simulation work in the industry
<br> <br> <img width="1958" height="1406" alt="image" src="https://github.com/user-attachments/assets/c8608447-95a2-4862-b4b6-6285d1800c91" />

## Project Introduction
* **Problem and Description**: The brain is fragile, and brief cerebral ischemia leads to brain injury; the cerebrovascular system is a critical system demanding urgent research. The cerebrovascular network is like a city's traffic system: the arterial network is responsible for "delivering" the freshest "takeout" (blood rich in oxygen and glucose) throughout the brain; the "home-delivery" capillary network is so dense that it is adjacent to every brain cell; after brain cells finish their "takeout," they release "trash" (carbon dioxide and waste), which is returned to the blood and recycled via the venous network. Its structure is akin to a vast underground water pipe network. Imaging data needs to be fine-grained; microvascular damage plays an important role in the impact of TBI. Imaging data needs to be complete, as the cerebrovascular system is an enormous system requiring systematic study. When all cerebral blood vessels, at any location, are clearly visible, high-definition, vascular researchers need it, clinicians need it (at a resolution unattainable by CT/MRI), and it is also needed for drug development, disease modeling, and blood flow simulation work. The limitations of *ex vivo* data cannot obscure its golden value of being whole-brain, complete, and high-resolution.

* **Task Division**: A collaborative project between the teams of Academician Zhuang Zhuo and Academician Luo Qingming/Professor Gong Hui. The former is responsible for physical injury experiments, which are part of a tens-of-millions-level military-industrial project; the latter is responsible for labeling/transgenic, biological, and imaging experiments, possessing imaging advantages (with work previously published in Science) and capable of obtaining *ex vivo* whole-brain high-resolution vascular data—a task very few institutions can accomplish. I am responsible for the subsequent image processing work, including preprocessing, segmentation, skeletonization, and network analysis.

* **Image Segmentation Data Scale**: Single data image size is $11400 \times 8000 \times 13200$. Whole-brain complete fine vasculature $\times 24$; including healthy / injured data.

* **Pain Points Caused by Massive Image Data Scale**: The massive scale of a single dataset and the volume of vascular data (on the order of $10^1$, $10^2$, $10^3$, $10^4$), brings enormous challenges to the requirements of segmentation accuracy. Manually labeling vessels and correcting errors in post-segmentation locations is practically impossible. Regardless of whether supervised or unsupervised segmentation methods are used, even a slight improvement is a huge boost for subsequent quantitative analysis, network analysis, and blood flow simulation.

* **Pain Points Caused by Image Data Characteristics**: Vessels exhibit 2D and 3D edge fractures, signal discontinuities, and interference signal issues. The data is 3D, the data volume is extremely large, and the vessel diameters span multiple orders of magnitude with complex structures.

* **Supervised Deep Learning Segmentation Methods**: A total of 19 models (not including those with poor performance). These include classic CV segmentation algorithms like VoxResNet, FCN, VNet; top-conference work specifically for tubular structures like DSCNet; common medical segmentation models like U-Net and nnUNet; segmentation models for medical cells and organs like nnFormer, UNETR++; and models using SAM as a primary module, such as MedSAM2, SAM2-UNet (2D stitching).

* **Superiority of Swin Transformer Method**: This work applies Swin Transformer to the task of cerebrovascular segmentation in the medical field. It uses hierarchical features to solve the "single-scale" problem; vessel diameters $5\mu m - 500\mu m$; suitable for dense segmentation tasks with multi-scale information. It uses efficient computation to solve the "computation explosion" problem; it uses windowed attention, reducing computational complexity from quadratic $O(N \times N)$ to linear $O(N \times 49)$; it is beneficial for processing large images, achieving good vessel edge segmentation, as large images can provide more effective non-redundant regional information. It uses shifted windows, W-MSA and SW-MSA, to increase the receptive field; a large receptive field can better understand the injury situation, whereas a small receptive field is akin to "viewing a leopard through a tube" (having a narrow view).

* **Problems Encountered with Swin Transformer Segmentation and Model Improvements**: Swin Transformer performs well in most locations, but it encounters a problem where a single vessel is segmented into multiple pieces, analogous to a line segment being broken into several sections. This work employs SENet to automatically learn which feature channels are more important, ensuring the integrity of vessel segmentation; uses $5 \times 1 \times 1$ convolutions to increase Z-direction connectivity; and uses $3 \times 3\ \times 3$ convolutional stacks to increase local connectivity, using these methods to solve the vessel fragmentation problem. Concurrently, Swin Transformer segmentation has a small amount of noise, and the added modules introduce checkerboard artifacts. This work uses a small-scale learning network for denoising and builds a complex checkerboard artifact removal model. Finally, ablation studies were conducted to verify the effectiveness of the added modules.

* **Zero-Shot Segmentation Methods**: The annotation process is highly dependent on expert knowledge, is time-consuming and labor-intensive, and has significant time and economic costs. It is difficult to unify the subjective judgments, experience levels, and operating standards of different annotators, inevitably leading to significant "inter-observer variability." At the same time, the data characteristics of different batches are not identical, and the transferability of supervised learning is insufficient. Foundation model methods are pursued to solve these problems; these types of models undergo large-scale training, and when encountering new data with new features, they can use zero-shot, few-shot, and other means for fine-tuning to quickly achieve relatively ideal results. This work studied zero-shot learning methods such as SAM2, SAMURAI, vesselFM, etc., and carried out modifications and performance evaluations. vesselFM shows significant effects, only performing less than ideally at artifacts and vessel bifurcations.

* **Operating Environment**: The network is implemented using Pytorch. Experiments are trained in parallel on a server equipped with 4 NVIDIA A100 GPU 80GB, and inference is performed on 15 servers equipped with NVIDIA RTX 5000 32GB. Scripts are used to execute the entire cerebrovascular segmentation and analysis pipeline, including monitoring and management.

* **Evaluation Metrics**: Parameters such as Accuracy, Precision, Recall, F1 Score, Dice, clDice, HD, and HD95 are used for evaluation. The method of this study achieves the best results in Accuracy, F1 Score, Dice, and HD95, and is $1-2\%$ superior to all other methods on the important Dice metric.

* **Implementation of 24 Whole-Brain Segmentations and Applications**: Analysis was performed from multiple dimensions, including length density, bifurcation point density, vessel angles, subgraph structures, and loop structures. The results show significant differences in multiple parameters between the injured and control groups. Classified by brain region, there are two types of vascular injury modes: localized damage and overall sparsity.
