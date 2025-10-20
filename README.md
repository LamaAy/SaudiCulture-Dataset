# 🇸🇦 SaudiCulture: Cultural Competence Benchmark for LLMs

[![Dataset](https://img.shields.io/badge/Dataset-441_Questions-green.svg)](data/)
[![Paper](https://img.shields.io/badge/Published_JKSU-10.1007%2Fs44443--025--00137--9-blue.svg)](https://doi.org/10.1007/s44443-025-00137-9)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)

> **A comprehensive benchmark dataset for evaluating Large Language Models' cultural competence within the diverse geographical and cultural contexts of Saudi Arabia.**

---

## 🌟 Key Features

- **🗺️ Multi-Regional Coverage**: 5 major Saudi regions (West, East, South, North, Center) + General questions  
- **🎭 Cultural Diversity**: 8 domains including food, clothing, entertainment, celebrations, crafts, architecture, language, and dating customs  
- **📝 Multiple Formats**: Open-ended, single-choice, and multiple-choice questions  
- **✅ Expert Validated**: Rigorously reviewed by cultural experts and native speakers  
- **📊 Comprehensive**: 441 culturally-rich questions with varying complexity levels  

---

## 👥 Authors

**Lama Ayash** (Corresponding Author)  
📧 Lama.Ayash@outlook.sa  
🏢 Department of Computer Science, King Khalid University, Abha, Saudi Arabia  
🔗 ORCID: [0000-0002-6268-9072](http://orcid.org/0000-0002-6268-9072)

**Hassan Alhuzali**  
📧 hrhuzali@uqu.edu.sa  
🏢 Department of Computer Science & Artificial Intelligence, Umm Al-Qura University, Makkah, Saudi Arabia

**Ashwag Alasmari**  
📧 aasmry@kku.edu.sa  
🏢 Department of Computer Science & Center for Artificial Intelligence (CAI), King Khalid University, Abha, Saudi Arabia

**Sultan Aloufi**  
📧 sdoufi@taibahu.edu.sa  
🏢 Department of Arabic Language, Taibah University, Medina, Saudi Arabia

---

## 📊 Dataset Overview

The dataset comprises **six regions** (five geographical + general cross-regional) and spans multiple cultural domains and question formats.  
Below are automatically generated statistics from the cleaned dataset (v3).

### 🗺️ Region Overview (v3)

| Region | Questions |
|--------|-----------:|
| **West** | 74 |
| **East** | 67 |
| **South** | 84 |
| **North** | 54 |
| **Center** | 76 |
| **General** | 86 |
| **Total** | **441** |

---

### 🧭 Domain by Region (v3)

| Region | Food | Entertainment | Clothing | Celebrations | Crafts | Architecture | Language | Dating |
|--------|------:|---------------:|-----------:|---------------:|----------:|--------------:|-----------:|---------:|
| **West** | 20 | 10 | 8 | 9 | 8 | 7 | 6 | 6 |
| **East** | 19 | 9 | 7 | 8 | 7 | 6 | 6 | 5 |
| **South** | 24 | 13 | 10 | 10 | 9 | 7 | 6 | 5 |
| **North** | 15 | 8 | 6 | 6 | 5 | 5 | 5 | 4 |
| **Center** | 21 | 10 | 8 | 9 | 8 | 7 | 7 | 6 |
| **General** | 26 | 11 | 7 | 8 | 8 | 7 | 10 | 9 |

> *Counts represent number of questions mapped per domain.*

---

### 🏷️ Category by Region (v3)

| Region | Common | Specialized | Cross-Regional |
|--------|--------:|-------------:|----------------:|
| **West** | 41 | 33 | 0 |
| **East** | 35 | 32 | 0 |
| **South** | 47 | 37 | 0 |
| **North** | 27 | 27 | 0 |
| **Center** | 42 | 34 | 0 |
| **General** | 0 | 0 | 86 |

> *“Common” refers to widely known cultural facts, while “Specialized” represents region-specific knowledge.*

---

### ❓ Question Type by Region (v3)

| Region | Open-Ended | Single-Choice | Multiple-Choice |
|--------|-------------:|----------------:|-----------------:|
| **West** | 18 | 38 | 18 |
| **East** | 15 | 35 | 17 |
| **South** | 20 | 40 | 24 |
| **North** | 12 | 29 | 13 |
| **Center** | 19 | 38 | 19 |
| **General** | 21 | 44 | 21 |

---

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/yourusername/saudi-culture-dataset.git
cd saudi-culture-dataset

```




---

## 🎯 Cultural Categories

| Category | Description | Sample Count |
|----------|-------------|--------------|
| **🍽️ Food** | Traditional dishes, culinary customs | 125 |
| **🎭 Entertainment** | Folk arts, traditional games | 95 |
| **🏺 Craft & Work** | Traditional handicrafts | 60 |
| **💬 Language & Communication** | Dialects, expressions | 42 |
| **💝 Dating** | Social customs, marriage traditions | 34 |
| **👘 Clothing** | Traditional attire, regional variations | 32 |
| **🎉 Celebrations** | Festivals, cultural events | 30 |
| **🏛️ Architecture** | Building styles, historical structures | 23 |

---

## 📈 Benchmark Results

### Model Performance by Region
| Model | West | East | South | North | Center | General | Overall |
|-------|------|------|-------|-------|---------|---------|---------|
| **GPT-4** | 66% | 52% | 56% | 36% | 51% | 69% | **55%** |
| **DeepSeek** | 51% | 39% | 37% | 47% | 40% | 58% | **45%** |
| **Llama 3.3** | 39% | 41% | 44% | 34% | 34% | 64% | **43%** |
| **AceGPT** | 25% | 27% | 38% | 28% | 27% | 45% | **32%** |
| **FANAR** | 25% | 17% | 26% | 30% | 25% | 34% | **26%** |
| **Jais** | 24% | 17% | 22% | 16% | 27% | 39% | **24%** |

### Performance by Question Format
- **Open-ended**: Most challenging (avg. 24% accuracy)
- **Single-choice**: Moderate difficulty (avg. 45% accuracy)  
- **Multiple-choice**: Highest accuracy (avg. 52% accuracy)

### Key Findings
- **Regional Variation**: Western region showed highest accuracy (66% for GPT-4), while Northern region was most challenging (16% for Jais)
- **Format Impact**: Multiple-choice questions facilitated higher accuracy due to constrained response space
- **Cultural Categories**: Crafts & work achieved highest accuracy (75% for GPT-4), while dating customs were most challenging

---

## 🎓 Research & Citation

### 📖 Publication
**Ayash, L., Alhuzali, H., Alasmari, A., & Aloufi, S.**  
*SaudiCulture: A benchmark for evaluating large language models’ cultural competence within Saudi Arabia.*  
**Journal of King Saud University – Computer and Information Sciences**, **37**, 123 (2025).  
📅 *Received:* March 15, 2025 | *Accepted:* June 22, 2025 | *Published:* July 21, 2025  
🔗 **DOI:** [10.1007/s44443-025-00137-9](https://doi.org/10.1007/s44443-025-00137-9)

### 📘 Citation (BibTeX)
```bibtex
@article{ayash2025saudiculture,
  title        = {SaudiCulture: A benchmark for evaluating large language models’ cultural competence within Saudi Arabia},
  author       = {Ayash, Lama and Alhuzali, Hassan and Alasmari, Ashwag and Aloufi, Sultan},
  journal      = {Journal of King Saud University - Computer and Information Sciences},
  volume       = {37},
  pages        = {123},
  year         = {2025},
  publisher    = {Elsevier},
  doi          = {10.1007/s44443-025-00137-9}
}
```

---

## 🙏 Acknowledgments

- **Cultural Experts:** Native Saudi reviewers from all five regions  
- **Funding:**  
  - Umm Al-Qura University (Grant: 25UQU4320430GSSR01)  
  - King Khalid University (Grant: RGP1/337/45)  
- **Data Sources:** [Saudipedia](https://saudipedia.com/) and expert contributions  
- **Special Thanks:** Walaa Al-Mukhtar, Saja Alhirbish, Khalid Alessa, and Manal Algethami  

---

## 🌍 Impact & Applications

- **Cultural AI Research:** Advancing understanding of cultural competence in AI  
- **Arabic NLP:** Improving cultural awareness in Arabic language models  
- **Educational Tools:** Supporting cultural education and awareness  
- **Industry Applications:** Enhancing culturally-aware AI products and services  

---

*This dataset represents a step towards more inclusive and culturally-aware artificial intelligence systems that can better serve diverse global communities.*
