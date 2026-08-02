markdown
# Yahoo Finance Medallion Pipeline

End-to-end stock market data pipeline on Azure using ADF, Databricks, and Medallion architecture.

## Architecture
Yahoo Finance API
↓
Azure Data Factory (Ingestion)
↓
Bronze Layer (Raw JSON in ADLS)
↓
Databricks Silver (Cleaned Delta)
↓
Databricks Gold (Aggregated KPIs)
↓
Dashboard (Power BI / Databricks SQL)

text

## Tech Stack

- **Azure Data Factory** - API ingestion
- **Azure Databricks** - PySpark transformations
- **Azure Data Lake Storage (ADLS)** - Delta Lake storage
- **Delta Lake** - ACID transactions
- **Power BI / Databricks SQL** - Dashboard visualization

## Repository Structure
yahoo-finance-medallion-pipeline/
├── README.md
├── arm-template/
│ ├── YAHOO_API_TO_ADLS.json ← ADF pipeline ARM template
│ └── manifest.json ← Pipeline visual metadata
├── notebooks/
│ └── (Coming soon - Databricks notebooks)
└── dashboard/
└── (Coming soon - Dashboard screenshots)

text

## Features

- ✅ Real-time Yahoo Finance API ingestion via ADF
- ✅ Medallion architecture (Bronze → Silver → Gold)
- ✅ Turnover percentage calculation
- ✅ Holding percentage analysis
- ✅ Volatility tracking
- ✅ Interactive dashboards

## Deployment Instructions

### Prerequisites
- Azure subscription
- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks workspace

### Deploy ADF Pipeline

1. Go to Azure Data Factory → Manage → ARM Template
2. Click "Import ARM Template"
3. Upload `arm-template/YAHOO_API_TO_ADLS.json`
4. Configure linked services:
   - `stockdataapi` → Yahoo Finance REST API
   - `ADLS_MyStorage` → Your ADLS Gen2 storage
5. Deploy and run the pipeline

## Author

Shantanu Kulkarni

## License

MIT

