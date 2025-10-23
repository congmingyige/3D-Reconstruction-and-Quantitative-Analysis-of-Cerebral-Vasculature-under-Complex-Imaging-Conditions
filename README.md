# 3D Reconstruction and Quantitative Analysis of Cerebral Vasculature under Complex Imaging Conditions
复杂图像条件下脑血管三维重建与定量分析 PPT等内容

本人正积极寻求合适的工作机会，若您有相关岗位推荐或招聘需求，欢迎通过邮箱1249591860@qq.com与我联系，期待与您沟通！

版本1 陈冠斌_PPT_联影_分子影像事业部算法_二面_20251023：比较全的一个版本

版本2 陈冠斌_复杂图像条件下脑血管三维重建与定量分析_最新的版本_但是有不少待添加的内容_20251023.pptx：最新的版本，相比版本1有不少新内容，也有不少内容是待添加的内容（PPT上标注有红色TBD的所在页）。因为最近比较忙，毕竟在找工作，面试也挺多，所以更新可能会比较慢，如果有快速更新期待和需求的话，请联系我。


# PPT下载链接
阿里云盘：https://www.alipan.com/s/PNWLD9AJZvw

夸克云盘：https://pan.quark.cn/s/c100a99df184

百度网盘：https://pan.baidu.com/s/1hp6YO0RXzVHWLTN_Nlm_tw?pwd=0000

## 欢迎学术上的任何交流，特别是关于医学图像处理、脑血管、分割、网络分析、血流模拟的内容，通过邮箱1249591860@qq.com或者GitHub Issues联系我即可

## 数据信息
**庞大数据集**：全脑完整精细血管 X 24

离体数据

**所有**脑血管、**任何位置**都能清晰可见，**高清无码**

**毛细血管分辨率** 0.35 x 0.35 x 1 μm

标记：FITC / Dylight

单个数据图像大小：11400 x 8000 x 13200

灰度值：8bit，0 - 255

预处理 + 配准

有监督方法：
  - 方法：**Swin Transformer + 5个解决分割断裂/去噪的模块；Accuracy、F1、Dice、HD95参数效果最优**
  - 数据集：600 / 400个160 x 160 x 160大小的1 x 1 x 1 μm的数据块。大致按照训练集 / 测试集 / 验证集 8 : 1 : 1的比例
  - 训练：A100 * 1
  - 推理：RTX 5000 * 15，同时并行跑多套数据和多个任务，附带健壮性脚本
  
无监督方法： vesselFM（**也是很强烈推荐他组的这个工作**）

## 展示
<img width="1750" height="775" alt="image" src="https://github.com/user-attachments/assets/6b43e0cf-5d8d-4bff-956d-5f4befb096ae" />

<img width="909" height="369" alt="image" src="https://github.com/user-attachments/assets/10098c93-8993-4e43-b1be-86760b96dd44" />

<img width="539" height="67" alt="image" src="https://github.com/user-attachments/assets/dada5612-7e7c-4fa2-af7f-080e06a18dd9" />

<img width="4400" height="2971" alt="该研究工作流程图" src="https://github.com/user-attachments/assets/e98ff8b6-cd0e-4237-bc3c-d935c94436fb" />

分割模块带来了新的棋盘格伪影
<img width="1214" height="1461" alt="image" src="https://github.com/user-attachments/assets/be1821c8-8745-4658-b6d3-85e8126c18a0" />

<img width="1422" height="812" alt="image" src="https://github.com/user-attachments/assets/64990791-682c-4639-b667-646ce20f2252" />

<img width="2754" height="983" alt="image" src="https://github.com/user-attachments/assets/a58a9fed-1d82-44ee-83b1-309c1b52234a" />

<img width="2712" height="970" alt="image" src="https://github.com/user-attachments/assets/6b95bca2-531d-440d-9593-3984f97d80b1" />

<img width="2087" height="1368" alt="image" src="https://github.com/user-attachments/assets/d1f54d7c-f6ea-40bd-9783-e79460960f44" />

<img width="2738" height="1195" alt="image" src="https://github.com/user-attachments/assets/cc3b93a9-3ae0-45e6-aeab-899520f01288" />

业界做血流模拟的工作
<img width="1958" height="1406" alt="image" src="https://github.com/user-attachments/assets/c8608447-95a2-4862-b4b6-6285d1800c91" />



