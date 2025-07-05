# 🇸🇦 SaudiCulture: Cultural Competence Benchmark for LLMs


[![Dataset](https://img.shields.io/badge/Dataset-441_Questions-green.svg)](data/)
[![Paper](https://img.shields.io/badge/Paper-Journal_of_King_Saud_University-blue.svg)](https://doi.org/10.1007/s44443-025-00137-9)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)

> **A comprehensive benchmark dataset for evaluating Large Language Models' cultural competence within the diverse geographical and cultural contexts of Saudi Arabia.**

## 🌟 Key Features

- **🗺️ Multi-Regional Coverage**: 5 major Saudi regions (West, East, South, North, Center) + General questions
- **🎭 Cultural Diversity**: 8 domains including food, clothing, entertainment, celebrations, crafts, architecture, language, and dating customs
- **📝 Multiple Formats**: Open-ended, single-choice, and multiple-choice questions
- **✅ Expert Validated**: Rigorously reviewed by cultural experts and native speakers
- **📊 Comprehensive**: 441 culturally-rich questions with varying complexity levels

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

## 📊 Dataset Overview

| Region | Questions | Cultural Categories | Complexity Levels |
|--------|-----------|-------------------|------------------|
| **West** | 74 | 8 categories | Common + Specialized |
| **East** | 67 | 8 categories | Common + Specialized |
| **South** | 84 | 8 categories | Common + Specialized |
| **North** | 54 | 8 categories | Common + Specialized |
| **Center** | 76 | 8 categories | Common + Specialized |
| **General** | 86 | 8 categories | Cross-regional |
| **Total** | **441** | **8** | **2** |

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/yourusername/saudi-culture-dataset.git
cd saudi-culture-dataset
pip install -r requirements.txt
```

### Basic Usage
```python
from saudiculture import SaudiCultureBenchmark

# Load the benchmark
benchmark = SaudiCultureBenchmark()

# Get questions by region
west_questions = benchmark.get_questions(region="west")

# Evaluate a model
results = benchmark.evaluate(
    model_name="gpt-4",
    region="all",
    question_format="open-ended"
)

print(f"Overall Accuracy: {results.accuracy:.2%}")
```

### Command Line Interface
```bash
# Evaluate a model on specific region
python scripts/evaluate.py --model gpt-4 --region west --format all

# Generate performance report
python scripts/generate_report.py --results results/gpt4_evaluation.json

# Visualize regional performance
python scripts/visualize.py --type regional_comparison
```

## 📋 Dataset Structure

```
data/
├── raw/                          # Original collected data
├── processed/                    # Clean, formatted datasets
│   ├── saudiculture_full.json   # Complete dataset
│   ├── by_region/               # Region-specific files
│   └── by_category/             # Category-specific files
└── examples/                    # Sample questions for each region
```

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

## 🛠️ Development & Contribution

### Setting up Development Environment
```bash
# Clone and setup
git clone https://github.com/yourusername/saudi-culture-dataset.git
cd saudi-culture-dataset

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements-dev.txt

# Run tests
pytest tests/
```

### Contributing Guidelines
1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## 📚 Documentation

- **[Data Collection Methodology](docs/data_collection.md)**: How the dataset was created
- **[Evaluation Guide](docs/evaluation_guide.md)**: How to properly evaluate models
- **[Cultural Guidelines](docs/cultural_guidelines.md)**: Understanding Saudi cultural context
- **[API Reference](docs/api_reference.md)**: Complete API documentation

## 🎓 Research & Citation

### Paper
**"SaudiCulture: A benchmark for evaluating large language models' cultural competence within Saudi Arabia"**  
*Journal of King Saud University Computer and Information Sciences, 2025*

**DOI**: [10.1007/s44443-025-00137-9](https://doi.org/10.1007/s44443-025-00137-9)

### Citation
```bibtex
@article{ayash2025saudiculture,
  title={SaudiCulture: A benchmark for evaluating large language models' cultural competence within Saudi Arabia},
  author={Ayash, Lama and Alhuzali, Hassan and Alasmari, Ashwag and Aloufi, Sultan},
  journal={Journal of King Saud University Computer and Information Sciences},
  year={2025},
  publisher={Elsevier},
  doi={10.1007/s44443-025-00137-9}
}
```

## 💬 Community & Support

### Research Collaborations
- **Academic Institutions**: King Khalid University, Umm Al-Qura University, Taibah University
- **Research Areas**: Cultural AI, Arabic NLP, Cross-cultural Computing

### Get Help
- **📧 Email**: [saudiculture@project.org](mailto:saudiculture@project.org)
- **💬 Discussions**: [GitHub Discussions](https://github.com/yourusername/saudi-culture-dataset/discussions)
- **🐛 Issues**: [Report Issues](https://github.com/yourusername/saudi-culture-dataset/issues)

## 🔗 Related Work

This work builds upon and extends previous cultural benchmarks:
- **ArabCulture** (Sadallah et al., 2025): Arabic cultural reasoning
- **AraDiCE** (Mousi et al., 2024): Dialectal and cultural capabilities
- **CulturalBench** (Chiu et al., 2024): Cross-cultural knowledge assessment

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Cultural Experts**: Native Saudi reviewers from all five regions
- **Funding**: 
  - Umm Al-Qura University (Grant: 25UQU4320430GSSR01)
  - King Khalid University (Grant: RGP1/337/45)
- **Data Sources**: [Saudipedia](https://saudipedia.com/) and expert contributions
- **Special Thanks**: Walaa Al-Mukhtar, Saja Alhirbish, Khalid Alessa, and Manal Algethami

## 📅 Publication Timeline

- **Received**: March 15, 2025
- **Accepted**: June 22, 2025
- **Dataset Release**: Upon paper acceptance

## 🌍 Impact & Applications

- **Cultural AI Research**: Advancing understanding of cultural competence in AI
- **Arabic NLP**: Improving cultural awareness in Arabic language models
- **Educational Tools**: Supporting cultural education and awareness
- **Industry Applications**: Enhancing culturally-aware AI products and services

---

**Made with ❤️ for advancing cultural understanding in AI**

*This dataset represents a step towards more inclusive and culturally-aware artificial intelligence systems that can better serve diverse global communities.*
