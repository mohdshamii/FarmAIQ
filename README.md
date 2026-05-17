<div align="center">

# FarmAIQ

### Smart Agriculture Recommendation System

*Empowering Farmers with AI-Driven Insights for Sustainable Farming*

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Machine Learning](https://img.shields.io/badge/ML-RandomForest%20%7C%20CNN-2E9C34?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Streamlit](https://img.shields.io/badge/Framework-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://kaggle.com)
[![License](https://img.shields.io/badge/License-MIT-F7DC6F?style=for-the-badge)](LICENSE)

</div>

---

## Overview

FarmAIQ is a machine learning-powered agriculture advisory platform that bridges the gap between data science and practical farming. It provides real-time, evidence-based recommendations across three critical domains — crop selection, fertilizer planning, and plant disease detection — enabling farmers to make informed decisions that improve yield, reduce waste, and promote sustainable land use.

The system ingests soil nutrient data, meteorological parameters, and plant imagery to generate actionable insights through a clean, accessible web interface built on Streamlit. Each recommendation is driven by models trained on curated agricultural datasets, achieving production-grade accuracy.

<div align="center">
  <img src="img/dashboard.png" width="800" alt="FarmAIQ Dashboard"/>
  <br/>
  <sub>The FarmAIQ dashboard — a unified control center for all three advisory modules</sub>
</div>

---

## Key Capabilities

### Crop Recommendation

FarmAIQ analyzes soil macronutrient composition (Nitrogen, Phosphorus, Potassium) alongside ambient environmental data to determine the crop most likely to thrive under given conditions. Rather than relying on generalized calendars or regional averages, recommendations are computed dynamically per input, accounting for the precise interaction between soil chemistry and climate variables.

<div align="center">
  <img src="img/pred1.png" width="420" alt="Crop Recommendation Input"/>
  <img src="img/pred2.png" width="420" alt="Crop Recommendation Output"/>
  <br/>
  <sub>Left: soil and weather parameter input form — Right: ranked crop recommendation output</sub>
</div>

### Plant Disease Detection

The disease detection module accepts leaf photographs and classifies visible symptoms across dozens of plant conditions using a Convolutional Neural Network. Early and accurate identification allows farmers to initiate targeted treatment before infections spread, reducing both crop loss and unnecessary pesticide use.

<div align="center">
  <img src="img/leaf1.png" width="420" alt="Healthy Leaf Analysis"/>
  <img src="img/leaf2.png" width="420" alt="Diseased Leaf Detection"/>
  <br/>
  <sub>Left: healthy leaf classification — Right: disease identified with treatment advisory</sub>
</div>

### Fertilizer Advisory

The fertilizer module compares actual soil nutrient readings against crop-specific optimal thresholds and surfaces a prioritized list of recommended inputs. It accounts for both deficiency and excess conditions, preventing over-application that degrades soil health and downstream water quality.

<div align="center">
  <img src="img/smartfert.png" width="800" alt="Smart Fertilizer Recommendation"/>
  <br/>
  <sub>Nutrient gap analysis driving fertilizer recommendations</sub>
</div>

### Weather Insights

Integrated weather data provides contextual climate information relevant to planting windows, irrigation scheduling, and disease risk conditions. Environmental readings are incorporated directly into recommendation logic, not treated as supplementary data.

<div align="center">
  <img src="img/weather.png" width="800" alt="Weather Insights Panel"/>
  <br/>
  <sub>Real-time weather context integrated into crop and disease advisory</sub>
</div>

### AI Crop Detection

Beyond the soil-parameter-based recommender, FarmAIQ includes an image-based crop detection feature that can identify crop type and growth stage from field photographs — useful for field auditing and multi-farm management workflows.

<div align="center">
  <img src="img/aicrop.png" width="800" alt="AI Crop Detection"/>
  <br/>
  <sub>Vision-based crop identification from field imagery</sub>
</div>

---

## Performance

| Module | Model | Validation Accuracy |
|---|---|---|
| Crop Recommendation | Random Forest Classifier | 99% |
| Disease Detection | Convolutional Neural Network (CNN) | 98% |
| Fertilizer Advisory | Rule-augmented Classification | — |

<div align="center">
  <img src="img/stats.png" width="800" alt="Model Performance Statistics"/>
  <br/>
  <sub>Training and validation performance metrics across all models</sub>
</div>

---

## Technology Stack

| Layer | Technology |
|---|---|
| Application Framework | Streamlit |
| Machine Learning | Scikit-learn (Random Forest) |
| Deep Learning | TensorFlow / Keras (CNN) |
| Data Processing | Pandas, NumPy |
| Language | Python 3.8+ |
| Dataset Source | Kaggle |

---

## Project Structure

```
FarmAIQ/
│
├── app.py                  # Streamlit application entry point
├── requirements.txt        # Python dependency manifest
│
├── models/                 # Serialized trained model files
│   ├── crop_model.pkl
│   ├── disease_model.h5
│   └── fertilizer_model.pkl
│
├── data/                   # Raw and preprocessed datasets
│   ├── crop_data.csv
│   └── fertilizer_data.csv
│
├── img/                    # Application screenshots and assets
└── README.md
```

---

## Installation

Clone the repository and set up the environment in a single command:

```bash
git clone https://github.com/codexshami/FarmAIQ.git && cd FarmAIQ && python -m venv venv && (venv\Scripts\activate || source venv/bin/activate) && pip install -r requirements.txt && streamlit run app.py
```

Or step by step:

```bash
# 1. Clone the repository
git clone https://github.com/codexshami/FarmAIQ.git
cd FarmAIQ

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # macOS / Linux
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the application
streamlit run app.py
```

The application will be available at `http://localhost:8501` in your browser.

---

## Contributing

Contributions are welcome. To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature-name`)
3. Commit your changes with clear, descriptive messages
4. Push the branch and open a Pull Request against `main`

Please ensure new features include appropriate test coverage and that existing tests pass before submitting a PR.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for full terms.

---

<div align="center">

Built by [Codexshami](https://github.com/codexshami)

If this project is useful to you, consider leaving a star on the repository.

</div>
