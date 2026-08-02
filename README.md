# 🎯 Smart Money Concepts V3.1.6 — Liquidity Probability Engine

![Pine Script Version](https://img.shields.io/badge/Pine_Script-v6-blue?style=for-the-badge&logo=tradingview)
![TradingView](https://img.shields.io/badge/TradingView-Indicator-00897B?style=for-the-badge&logo=tradingview)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

An algorithmic **Smart Money Concepts (SMC) Target Prediction & Probability Scoring Engine** written in **Pine Script v6** for TradingView.

V3.1.6 processes structural liquidity zones through a **12-factor weighted scoring model (0–100%)** to rank, project, and predict which liquidity targets have the highest probability of being swept by institutional order flow.

---

## 🔥 Key Features

* **⚖️ 12-Factor Weighted Probability Engine:** Dynamically scores liquidity zones across multiple technical metrics:
  * *Distance to Price (20%)*
  * *Trend Alignment (15%)*
  * *Market Regime / ADX Strength (10%)*
  * *Structure Quality (10%)*
  * *Liquidity Quality (10%)*
  * *Priority Level (10%)*
  * *Swing Strength, Volume, Momentum, Volatility, Test History & Age (25% total)*
* **🥇 Multi-Tier Target Ranking:** Automatically ranks targets into **Primary (Rank 1)**, **Secondary (Rank 2)**, and **Third (Rank 3)** target levels based on calculated probability ratings.
* **🎨 Dynamic Probability Heatmap:** Renders color-coded target lines and chart labels (ranging from red/weak to green/institutional) reflecting real-time confidence scores.
* **📊 Prediction Status Dashboard:** On-screen HUD displaying probability trends, prediction confidence %, target ATR distances, and model accuracy metrics.
* **🔌 Open Output API:** Exposes standardized prediction variables (`export_PrimaryTarget`, `export_ProbabilityScore`, `export_PredictionConfidence`) for external EAs, webhooks, or automated execution scripts.

---

## 📊 Dashboard Overview

The built-in realtime prediction status dashboard displays key predictive metrics:

| Metric | Description |
| :--- | :--- |
| **Primary Target (Rank 1)** | Highest probability liquidity price level currently projected |
| **Probability Score** | Multi-factor weighted percentage score (0–100%) and classification |
| **Probability Trend** | Tracks realtime momentum shifts in target probability (*Increasing, Decreasing, Stable*) |
| **Prediction Confidence** | Consolidated confidence index incorporating ADX trend strength |
| **Secondary & Third Targets** | Alternative liquidity targets for multi-take-profit trade planning |
| **Target Distance (ATR)** | Normalization of target distance relative to market volatility |

---

## 🛠️ Configuration & Settings

### 1. Probability Scoring Weights (Customizable up to 100%)
Users can adjust the specific weights given to each market factor:
* `Distance Weight` *(Default: 20)*
* `Trend Alignment Weight` *(Default: 15)*
* `Market Regime / ADX Weight` *(Default: 10)*
* `Structure & Liquidity Quality Weights` *(Default: 10 each)*
* `Auxiliary Weights` *(Volume, Momentum, Volatility, Tests, Age)*

### 2. Prediction Engine Settings
* `Pivot Length` *(Default: 10)*: Structural swing detection length.
* `Minimum Target Probability Threshold` *(Default: 70%)*: Minimum score required to classify a zone as a high-probability target.

---

## 💻 Installation & Usage

1. Open **[TradingView](https://www.tradingview.com)**.
2. Open the **Pine Editor** tab at the bottom of your workspace.
3. Create a new script, clear the default code, and paste the code from `SMC_Probability_Engine_v3_1_6.pine`.
4. Click **Save** and then select **Add to Chart**.

---

## ⚡ Real-Time Alerts Included

Native TradingView alert triggers for automated webhook execution and notifications:
* 🔥 **High Probability Target Detected (Score ≥ 90%)**
* ⚡ **Target Probability Trend Increased**


---

## 📜 License

This project is open-source and released under the [MIT License](LICENSE).
