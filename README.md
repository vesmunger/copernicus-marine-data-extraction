# Copernicus Marine Data Extraction for Kenya EEZ

A modular Python script for extracting oceanographic and biogeochemical datasets from the Copernicus Marine Service, focused on the Kenya Exclusive Economic Zone (EEZ). This project enables automated subsetting of marine data for environmental analysis, research, and machine learning applications.

---

## 🌍 Project Overview

This project retrieves marine datasets such as nutrients, plankton, salinity, sea surface height, and temperature anomalies from the Copernicus Marine platform.

The extraction is spatially constrained to the **Kenya EEZ region** and temporally configurable, allowing flexible data acquisition for oceanographic studies and geospatial modeling.

---

## 📊 Datasets Covered

The script extracts the following variables:

| Category    | Variables                                                |
| ----------- | -------------------------------------------------------- |
| Nutrients   | Iron (Fe), Nitrate (NO₃), Phosphate (PO₄), Silicate (Si) |
| Plankton    | Chlorophyll (Chl), Phytoplankton (Phyc)                  |
| Physical    | Salinity (So), Sea Surface Height (ZOS)                  |
| Temperature | Sea Surface Temperature Anomaly                          |

---

## 📍 Spatial Coverage

* Longitude: 39.0 → 45.0
* Latitude: -5.0 → 1.25
* Depth: ~0.5m → 21.6m

👉 Focused on the **Kenyan coastal and EEZ region**

---

## ⏱️ Temporal Coverage

* Start Date: 2025-01-01
* End Date: 2025-01-02

This can be extended for long-term time series analysis.

---

## ⚙️ Features

* Automated extraction of multiple datasets
* Customizable spatial and temporal subsetting
* Structured and consistent file naming
* Modular configuration using dictionaries
* Supports dry-run mode for testing before download

---

## 🛠️ Installation

Install dependencies:

```bash
pip install copernicusmarine
```

Ensure you have access credentials for Copernicus Marine services.

---

## ▶️ Usage

Run the script:

```bash
python extract_data.py
```

### Dry Run Mode

By default:

```python
dry_run=True
```

This simulates the extraction without downloading data.

To download data:

```python
dry_run=False
```

---

## 📁 Output

Data will be saved to:

```text
C:\Users\ADMIN\marine\cmes_extraction\data
```

File naming format:

```text
{dataset_name}_kenyaeez_{start_date}_{end_date}
```

Example:

```text
nutrients_kenyaeez_20250101_20250102
```

---

## 🧩 Code Structure

* `dataset_dict` → maps dataset IDs to variables
* `dataset_name_dict` → user-friendly dataset names
* `subsetting_dict` → spatial, temporal, and output parameters
* `generate_filename()` → ensures consistent file naming
* Main loop → iterates through datasets and extracts data

---

## 🌐 Use Cases

* Oceanographic analysis
* Climate and environmental monitoring
* Marine ecosystem studies
* Fisheries and coastal management
* Input data for machine learning models (e.g., forecasting, anomaly detection)

---

## 🔮 Future Improvements

* Integration with xarray and rioxarray for post-processing
* Automated visualization of extracted datasets
* Support for batch temporal extraction (multi-year datasets)
* Integration with GIS tools (e.g., QGIS workflows)
* Deployment as a reusable data pipeline

---

## 📄 License

MIT
