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

## 使用指南
复杂图像条件下脑血管三维重建与定量分析PPT等内容

版本1 陈冠斌_PPT_联影_分子影像事业部算法_二面_20251023：比较全的一个版本

版本2 陈冠斌_复杂图像条件下脑血管三维重建与定量分析_最新的版本_但是有不少待添加的内容_20251023.pptx：最新的版本，相比版本1有不少新内容，也有不少内容是待添加的内容（PPT上标注有红色TBD的所在页）。因为最近比较忙，毕竟在找工作，面试也挺多，所以更新可能会比较慢，如果有快速更新期待和需求的话，请联系我。

本人正积极寻求合适的工作机会，若您有相关岗位推荐或招聘需求，欢迎通过邮箱1249591860@qq.com与我联系，期待与您沟通！

## PPT下载链接
阿里云盘：https://www.alipan.com/s/PNWLD9AJZvw

夸克云盘：https://pan.quark.cn/s/c100a99df184

百度网盘：https://pan.baidu.com/s/1hp6YO0RXzVHWLTN_Nlm_tw?pwd=0000

## 欢迎学术上的任何交流，特别是关于医学图像处理、脑血管、分割、网络分析、血流模拟的内容，通过邮箱1249591860@qq.com或者GitHub Issues联系我即可

## 关于本工作
庄茁院士（王鹏老师）和骆清铭院士、龚辉教授团队合作课题

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
