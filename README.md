# 🚘 Subjective Risk Annotation in Urban Driving Scenes (SRA-UDS)

This repository contains the **SRA-UDS dataset**, a richly annotated multimodal corpus of urban driving scenes with:

- 🚦 **Subjective risk scores** (1–5) annotated by 13 human annotators  
- 📜 **Natural language explanations** in **Japanese** (with optional English translation)  
- 🏷️ **Contextual tags** including driving environment and action descriptors  
- 🖼️ Associated driving **scene images** captured in urban areas of Japan  

This dataset is designed to support research in:
- Multimodal risk-aware scene understanding  
- Bilingual caption generation for autonomous driving  
- Explainable AI and VLMs for real-world mobility systems  

---

## 📁 Dataset Structure

Each data entry includes the following fields:

```json
{
  "scene_id": "CT000123",
  "image_path": "images/CT000123.jpg",
  "risk_score": 4,
  "explanation_ja": "前方の自転車が急に車道に出てきたため減速した。",
  "explanation_en": "Slowed down as a bicycle suddenly entered the lane.",
  "env_tags": ["residential", "rainy", "daytime"],
  "action_tags": ["braking", "lane keeping"]
}


## Directory Layout
```bash
.
├── data/
│   ├── annotations.json       # Full annotation file
│   ├── images/                # Folder of driving scene images
│   └── README_data.md         # Dataset-specific notes
├── models/                    # Model scripts (coming soon)
├── notebooks/                 # Usage examples in Colab/Jupyter
├── LICENSE
└── README.md
```

📦 Installation (Optional Toolkit)
```bash
git clone https://github.com/<your-org>/sra-uds.git
cd sra-uds
pip install -r requirements.txt

```

🚀 Quickstart Example
```python
from datasets import load_dataset

dataset = load_dataset("path/to/annotations.json", split="train")
sample = dataset[0]
print(sample["risk_score"], sample["explanation_ja"])
```

📜 License
This dataset is distributed under the Creative Commons Attribution 4.0 International License (CC BY 4.0), unless otherwise noted.

🧾 Citation
If you use this dataset in your research, please cite:

```bibtex
@article{bao2025srauds,
  title={Subjective Risk Annotation in Urban Driving Scenes},
  author={Bao, Naren    and others},
  journal={xxxx 2025 (under submission)},
  year={2025}
}
```

📬 Contact
For questions, collaborations, or suggestions:
- Naren Bao (University of Tokyo / AquaAge Inc.): naren@g.ecc.u-tokyo.ac.jp
- GitHub Issues or Discussions tab

