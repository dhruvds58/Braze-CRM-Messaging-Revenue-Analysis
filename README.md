# Braze CRM Messaging & Revenue Analysis

This project presents a full-funnel analysis of CRM messaging performance and its impact on purchase behavior using Braze customer engagement data. Conducted as part of a quarterly business review, the project leverages Google Cloud infrastructure, PySpark, and Python-based visualizations to identify key trends and deliver actionable insights for marketing and revenue teams.

## 🔍 Project Goals

- Analyze message performance across CRM channels: Email, Push, WhatsApp, SMS, In-App, and Content Cards
- Compare user engagement and revenue between customer segments (MNR vs O&D)
- Detect attribution and data quality issues in campaign metadata
- Provide strategic recommendations to optimize CRM performance

## 🛠️ Tech Stack

- **Google Cloud Platform (GCP)**: Storage and compute
- **Dataproc + PySpark**: Large-scale data processing
- **Pandas, Matplotlib, Seaborn**: EDA and visualization
- **SQL**: Preprocessing and joins
- **Jupyter Notebook**: Analytical environment for end-to-end analysis

## 📊 Key Insights

### Messaging Channel Performance
- **Email Click-to-Open Rate**: O&D = 9.2%, MNR = 1.85% (despite MNR sending 3.5x more emails)
- **Push Notification Open Rate** (Q4 2024): MNR = 4.1%, O&D = 1.6%
- **WhatsApp Delivery Rate**: O&D achieved 91% with 245K sends—14x more than MNR
- **In-App CTR** dropped to 31.8% from 42% last quarter, while Content Card CTR improved to 5.1%

### Purchase Behavior
- ~1M purchases occurred within 24 hours of interacting with a Braze message
- **Daily Revenue per User**: MNR = $65, O&D = $47
- **Lifetime Value per User**: MNR = $565, O&D = $135
- Total Lifetime Revenue = $1.8B

### Data Gaps & Structural Issues
- Key columns like `Canvas`, `Campaign`, and `Variation` were mostly empty
- Many negative purchase prices remained unexplained after time-based joins
- CRM messaging lacked structured orchestration (no unified Canvas or Campaign logic)

## ✅ Recommendations

- Apply **Send Optimization** and implement **Sunset Policy** for low-performing MNR emails
- Build structured messaging flows via Braze Canvas to support attribution and A/B testing
- Fix metadata gaps in CRM exports to improve segmentation and targeting
- Reconcile purchase logs by linking negative entries with return order IDs
