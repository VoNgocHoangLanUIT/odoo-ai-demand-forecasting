# Odoo AI Demand Forecasting

An ERP-focused project that integrates product demand forecasting into **Odoo** to support smarter procurement and inventory decisions.

## Overview

This project proposes and demonstrates an AI-integrated demand forecasting workflow inside **Odoo ERP**. Instead of relying on manual estimation, the system uses historical sales data and forecasting models to estimate future demand, then supports procurement planning through **RFQs**, **purchase decisions**, and **reordering rules**.

The project is built around a business scenario where inaccurate forecasting can lead to:
- **Stockouts** of critical items
- **Overstocking** of slow-moving products
- Higher carrying costs and less efficient working capital usage

The solution focuses on integrating AI into Odoo’s purchasing-related workflow, using historical sales data and forecasting models such as **XGBoost** and **Prophet**, while also comparing against traditional baselines like **Moving Average**, **SARIMA**, and **Holt-Winters**. It targets demand planning, procurement support, and inventory optimization in an ERP context.

## Objectives

- Analyze historical sales data and business factors affecting demand
- Build and compare forecasting models for short-term demand prediction
- Integrate forecast output into **Odoo** for procurement and inventory operations
- Support operational decisions such as:
  - Purchase planning
  - Reordering point setup
  - RFQ and PO preparation
  - Inventory control improvements
- Compare the **AS-IS** manual process with the **TO-BE** AI-assisted workflow

## Scope

### Business scope
The project focuses on ERP-related operations directly affected by demand forecasting:
- Purchasing / Procurement
- Sales
- Inventory Receiving
- Inventory Shipping

### Data scope
- Monthly sales dataset from **2020 to 2024**
- Forecasting targets built around planning SKUs / Region–Country combinations

### Technical scope
- Baseline models: Moving Average, Holt-Winters, SARIMA
- Main ML models: XGBoost, Prophet
- ERP integration with Odoo for operational support

## Project Workflow

1. **Business Understanding**
2. **Data Understanding**
3. **Data Preparation & EDA**
4. **Modeling & Evaluation**
5. **Export forecast results** for Odoo import
6. **Configure Odoo modules and master data**
7. **Apply reordering policy and procurement flow in Odoo**

## Main Features

- Demand forecasting for product planning
- Comparison between traditional forecasting and ML-based forecasting
- Odoo-oriented procurement support
- CSV export for Odoo import
- Vendor, product, and pricing setup for demo scenarios
- Reordering rules configuration in inventory/purchase flow
- End-to-end demo from forecast to purchasing process in Odoo

## Tech Stack

- **ERP Platform:** Odoo
- **Model Development:** Google Colab / Python
- **Forecasting Models:** Moving Average, SARIMA, Holt-Winters, XGBoost, Prophet
- **Data Processing:** CSV-based preprocessing and analysis
- **Business Modeling:** BPMN for AS-IS and TO-BE process design

## Evaluation Metrics

The project evaluates forecasting performance using:
- **MAE**
- **RMSE**
- **MAPE**
- **R²**

## Odoo Integration Idea

The forecast output is used to support Odoo operations by:
- Generating procurement recommendations
- Defining **Min/Max** reordering rules
- Supporting **RFQ / PO** creation
- Improving coordination between sales, inventory, and purchasing

The workflow can be implemented so that data is processed for forecasting, then returned to Odoo so users can make more informed operational decisions directly within the ERP environment.

## Repository Structure

```text
.
├── README.md
├── docs/                    # Report, screenshots, BPMN diagrams
├── data/                    # Input and processed datasets
├── notebooks/               # Colab / Jupyter notebooks for EDA and modeling
├── models/                  # Saved models or experiment artifacts
├── exports/                 # CSV files prepared for Odoo import
├── odoo/                    # Odoo-related configs, import templates, custom logic
└── assets/                  # Images used in the README or presentation
```

## Suggested Setup

```bash
git clone https://github.com/<your-username>/odoo-ai-demand-forecasting.git
cd odoo-ai-demand-forecasting
```

Typical local workflow:
1. Prepare the dataset
2. Run notebooks for preprocessing and forecasting
3. Export forecast results to CSV
4. Import products / vendors / rules into Odoo
5. Run procurement demo flow

## Suggested Repository Contents

To make the repository strong for GitHub and CV purposes, you should include:
- Final report PDF
- Dataset sample or anonymized sample
- Colab/Jupyter notebooks
- Export CSV samples for Odoo import
- BPMN diagrams
- Odoo screenshots for demo steps
- A short architecture diagram
- Optional: video demo or GIF walkthrough

## Team

- **Võ Ngọc Hoàng Lân** — Project Manager
- **Nguyễn Phúc Lộc** — Data Analyst / AI Engineer
- **Nguyễn Minh Hiển** — ERP Consultant
- **Võ Hồ Trung Quân** — Business Analyst

## Future Improvements

- Automate the full forecast-to-Odoo pipeline
- Extend forecasting to a broader supply chain scope
- Improve production readiness of the integration layer
- Explore deep learning models for larger datasets and more complex demand patterns

## Acknowledgment

This repository is based on the course project report:
**“Tích hợp mô hình dự báo nhu cầu sản phẩm vào hệ thống ERP cho ngành bán lẻ”** (IS336 - Hoạch định nguồn lực doanh nghiệp), UIT, 2025.
