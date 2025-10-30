<div align="center">

# 📐Pi-GPS:

## *Enhancing Geometry Problem Solving by Unleashing the Power of Diagrammatic Information*

<p align="center">
  <img src="https://img.shields.io/badge/ICCV-2025-red?style=for-the-badge&logo=ieee&logoColor=white" alt="ICCV 2025">
  <img src="https://img.shields.io/badge/Status-Accepted-brightgreen?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Paper-ArXiv-b31b1b?style=for-the-badge&logo=arxiv&logoColor=white" alt="Paper">
</p>

<p align="center">
  <a href="https://arxiv.org/abs/2503.05543">📄 Paper</a> •
  <a href="#-getting-started">🚀 Quick Start</a> •
  <a href="#-performance">📊 Results</a> •
  <a href="#-citation">📚 Citation</a>
</p>

---

</div>

## 🎉 Announcement

**🏆 This paper has been accepted at ICCV 2025!** 🎉

We're excited to share our work on geometry problem solving with the community!

---

## 👥 Authors

<div align="center">

**Junbo Zhao**<sup>1†</sup> • **Ting Zhang**<sup>1†✉</sup> • **Jiayu Sun**<sup>1</sup> • **Mi Tian**<sup>2</sup> • **Hua Huang**<sup>1✉</sup>

<sup>1</sup>Beijing Normal University　　<sup>2</sup>TAL

<sub>† Equal contribution　　✉ Corresponding author</sub>


</div>

---

## 📖 Overview

We propose **Pi-GPS**, a novel framework for geometry problem solving that leverages diagrammatic information to resolve textual ambiguities. Our approach combines multi-modal understanding with symbolic reasoning to achieve state-of-the-art performance.

<div align="center">
  <img src="images/framework.png" alt="Pi-GPS Framework" width="80%">
  <br>
  <em>📐 Framework Overview of Pi-GPS</em>
</div>

---

## 🔍 Key Features

<div align="center">

| Component | Description |
|-----------|-------------|
| 🔧 **Rectifier** | Utilizes multi-modal language models (MLLMs) to disambiguate text by incorporating diagrammatic context |
| ✅ **Verifier** | Ensures refined text adheres to geometric rules, effectively reducing model hallucinations |
| 🧠 **Symbolic Solver** | Combines neural parsing with symbolic reasoning for robust problem solving |

</div>

---

## 📊 Performance

🏆 **Pi-GPS achieves state-of-the-art results**, outperforming previous neural-symbolic methods by nearly **10%** on standard benchmarks!

<div align="center">
  <table border="1" cellspacing="0" cellpadding="5">
    <thead>
      <tr>
        <th rowspan="2">Category</th>
        <th rowspan="2">Method</th>
        <th colspan="2">Geometry3K</th>
        <th colspan="2">PGPS9K</th>
      </tr>
      <tr>
        <th>Completion</th>
        <th>Choice</th>
        <th>Completion</th>
        <th>Choice</th>
      </tr>
    </thead>
    <tbody>
      <!-- MLLMs -->
      <tr>
        <td rowspan="4">MLLMs</td>
        <td>Qwen-VL</td>
        <td>22.1</td>
        <td>26.7</td>
        <td>20.1</td>
        <td>23.2</td>
      </tr>
      <tr>
        <td>GPT-4o</td>
        <td>34.8</td>
        <td>58.6</td>
        <td>33.3</td>
        <td>51.0</td>
      </tr>
      <tr>
        <td>Claude 3.5 Sonnet</td>
        <td>32.0</td>
        <td>56.4</td>
        <td>27.6</td>
        <td>45.9</td>
      </tr>
      <tr>
        <td>Gemini 2</td>
        <td>38.9</td>
        <td>60.7</td>
        <td>38.2</td>
        <td>56.8</td>
      </tr>
      <!-- Neural Methods -->
      <tr>
        <td rowspan="6">Neural Methods</td>
        <td>NGS</td>
        <td>35.3</td>
        <td>58.8</td>
        <td>34.1</td>
        <td>46.1</td>
      </tr>
      <tr>
        <td>Geoformer</td>
        <td>36.8</td>
        <td>59.3</td>
        <td>35.6</td>
        <td>47.3</td>
      </tr>
      <tr>
        <td>SCA-GPS</td>
        <td>-</td>
        <td>76.7</td>
        <td>-</td>
        <td>-</td>
      </tr>
      <tr>
        <td>GOLD<sup>*</sup></td>
        <td>-</td>
        <td>62.7</td>
        <td>-</td>
        <td>60.6</td>
      </tr>
      <tr>
        <td>PGPSNet-v2-S<sup>*</sup></td>
        <td>65.2</td>
        <td>76.4</td>
        <td>60.3</td>
        <td>69.2</td>
      </tr>
      <tr>
        <td>LANS (Diagram GT)<sup>*</sup></td>
        <td>72.1</td>
        <td>82.3</td>
        <td>66.7</td>
        <td>74.0</td>
      </tr>
      <!-- Neural-symbolic Methods -->
      <tr>
        <td rowspan="4">Neural-symbolic Methods</td>
        <td>Inter-GPS</td>
        <td>43.4</td>
        <td>57.5</td>
        <td>-</td>
        <td>-</td>
      </tr>
      <tr>
        <td>GeoDRL</td>
        <td>57.9</td>
        <td>68.4</td>
        <td>55.6</td>
        <td>66.7</td>
      </tr>
      <tr>
        <td>E-GPS</td>
        <td>-</td>
        <td>67.9</td>
        <td>-</td>
        <td>-</td>
      </tr>
      <tr>
        <td>Pi-GPS (ours)</td>
        <td><b>70.6</b></td>
        <td><b>77.8</b></td>
        <td><b>61.4</b></td>
        <td><b>69.8</b></td>
      </tr>
    </tbody>
  </table>
</div>

---

## 🚀 Getting Started

### 📋 Prerequisites

<div align="center">

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-Latest-red?style=flat-square&logo=pytorch&logoColor=white)

</div>

### 📥 Installation

```bash
# Clone the repository
git clone https://github.com/hellozting/Pi-GPS.git
cd Pi-GPS

# Install dependencies
pip install -r requirements.txt
```

### 📊 Dataset Preparation

We use two standard geometry datasets:

<div align="center">

| Dataset | Link | Description |
|---------|------|-------------|
| 📐 **Geometry3K** | [Download](https://lupantech.github.io/inter-gps/#Dataset) | 3K geometry problems with diagrams |
| 📊 **PGPS9K** | [Download](https://nlpr.ia.ac.cn/databases/CASIA-PGPS9K/) | 9K plane geometry problems |

</div>

Download and extract datasets:
```bash
# Extract images for unified processing
python data/extract.py
```

---

## ⚡ Quick Start

### 🎯 Run with Pre-processed Data

```bash
python Solver/test.py --label final
```

### 🛠️ Run from Scratch

<details>
<summary>Click to expand step-by-step instructions</summary>

#### 1️⃣ Text Parser
```bash
python Parser/text_parser.py
```

#### 2️⃣ Diagram Parser
Follow [PGDPNet](https://github.com/mingliangzhang2018/PGDP) setup instructions.

#### 3️⃣ Disambiguation Module
```bash
# Add points to images
python Disambiguation_module/addPointsToImage.py

# Set your MLLM API in Disambiguation_module/align.py
python Disambiguation_module/GuidedAlign.py
```

#### 4️⃣ Theorem Predictor
```bash
# Set your LLM API in Theorem_predictor/LLMPredict.py
python Theorem_predictor/LLMPredict.py
```

#### 5️⃣ Solver
```bash
python Solver/test.py --label final_result \
  --text_logic_form_path Disambiguation_module/disambiguated_text_logic_forms_pred.json \
  --diagram_logic_form_path Parser/diagram_parser/PGDP.json \
  --predict_path Theorem_predictor/LLM_pred_seq.json
```

</details>

---

## 📚 Citation

If you find our work helpful, please consider citing:

```bibtex
@InProceedings{Zhao_2025_ICCV,
    author    = {Zhao, Junbo and Zhang, Ting and Sun, Jiayu and Tian, Mi and Huang, Hua},
    title     = {Pi-GPS: Enhancing Geometry Problem Solving by Unleashing the Power of Diagrammatic Information},
    booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
    month     = {October},
    year      = {2025},
    pages     = {1526-1536}
}
```

---

## 🤝 Contributing

We welcome contributions! Please feel free to:

- 🐛 Report bugs
- 💡 Suggest features
- 📝 Improve documentation
- 🔧 Submit pull requests

---

## 🙏 Acknowledgments

<div align="center">

Our work builds upon several excellent projects:

[![Inter-GPS](https://img.shields.io/badge/Inter--GPS-Foundation-blue?style=flat-square)](https://github.com/lupantech/InterGPS)
[![PGDP](https://img.shields.io/badge/PGDP-Diagram%20Parser-green?style=flat-square)](https://github.com/mingliangzhang2018/PGDP)
[![GeoDRL](https://img.shields.io/badge/GeoDRL-Baseline-orange?style=flat-square)](https://aclanthology.org/2023.findings-acl.850/)

</div>

---

## 📞 Contact

<div align="center">

**Questions or suggestions?**

📧 [zhaojunbo@mail.bnu.edu.cn](mailto:zhaojunbo@mail.bnu.edu.cn)  
🐙 [Open an Issue](https://github.com/hellozting/Pi-GPS/issues)

---

<sub>Made with ❤️ by the Pi-GPS Team</sub>

</div>
