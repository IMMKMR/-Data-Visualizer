# 📊 Data Visualizer Platform

A premium, interactive data visualization suite designed for deep geographical and performance analytics. This platform transforms raw CSV/Excel datasets into rich, actionable insights through dynamic maps and intuitive dashboards.

## 🚀 Overview
The **Data Visualizer Platform** is built to handle complex hierarchical data (Zone > Region > State > District). It provides a seamless transition from raw spreadsheet data to high-fidelity geographical heatmaps and analytical charts, allowing users to identify trends, outliers, and performance metrics across India's geographical landscape.

---

## 🛠️ Data Processing & How It Works

### 1. Data Ingestion
The platform uses the `xlsx` library to parse `.csv`, `.xlsx`, and `.xls` files.
- **Multi-file Support**: You can upload multiple files sequentially.
- **Smart Mapping**: Upon upload, the platform intelligently guesses column roles (e.g., identifies "Sales" as a measure and "State" as a dimension).
- **Duplicate Detection**: When appending data, the system automatically fingerprints rows to identify and flag potential duplicates, giving you the choice to keep or skip them.

### 2. Processing Engine (`dataProcessor.js`)
Once data is uploaded:
- **Normalization**: Text is trimmed and normalized for consistent grouping.
- **Aggregation**: Data is automatically rolled up at various levels (National, Zonal, Regional, State, and District).
- **Quality Check**: The system generates a quality report, flagging missing values or inconsistent geographical mappings.

---

## 📄 Data Formatting (Sample CSV)

To get the most out of the system, your data should follow a structured format. Here are the top 5 columns and some sample data from the `Test data.csv`:

| District | State | Sales | Target | Territory | Region | Zone |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Nicobars | Andaman and Nicobar Islands | 6,275,884 | 10,441,876 | AND-South | All India | Global |
| North and Middle Andaman | Andaman and Nicobar Islands | 11,238,946 | 14,956,430 | AND-East | All India | Global |
| South Andaman | Andaman and Nicobar Islands | 8,734,718 | 11,104,388 | AND-East | All India | Global |
| Anantapur | Andhra Pradesh | 10,826,016 | 12,480,466 | AND-Central | All India | Global |
| Chittoor | Andhra Pradesh | 4,904,131 | 5,858,167 | AND-North | All India | Global |

---

## ✨ Key Features

### 📁 Multi-file Upload & Data Management
- **Append vs. Replace**: Upload fresh data to replace your current view or append it to building a larger historical dataset.
- **In-Platform Editing**: Correct typos or update values directly within the "Data Manager" table without re-uploading the file.
- **Status Toggle**: Temporarily disable specific rows from appearing in your charts and maps without deleting them.

### 💾 Workspace Saving
- Create independent **Workspaces** for different projects (e.g., "Q1 Sales" vs. "Inventory 2024").
- All settings—including uploaded data, filter states, and color preferences—are saved locally for instant recovery upon your next visit.

### 🎨 Color Editing & Themes
- **Dynamic Heatmaps**: Use the Properties Panel to choose from curated color gradients (e.g., Viridis, Magma, Plasma) or define your own stops.
- **Glassmorphism UI**: Switch between a sleek **Dark Mode** and a crisp **Light Mode**.

### 🗺️ Interactive Layers
- **Geographical Granularity**: Toggle between State-level and District-level views.
- **Custom Borders**: View State boundaries and District outlines independently.
- **Auto-Zoom**: Clicking a territory or filtering automatically pans and zooms the map to the relevant area.

### 📈 Analytics Tab
A dedicated space for non-geographical deep-dives:
- **Metric Cards**: Instant visibility into Total Sales, Average Performance, and Growth.
- **Trend Charts**: Visualise your measures across territories or time.
- **Distribution Histograms**: Understand data density and distribution.
- **Territory Rankings**: See top-performing and bottom-performing districts/states at a glance.

### 🔍 Advanced Filters
- **Global Slicing**: Use the persistent Filter Bar to slice data by Zone, Region, State, or Territory.
- **Sync**: Filters applied in the map view are instantly reflected in the Analytics tab and vice versa.

---

## 🛠️ Technology Stack
- **Frontend**: React (Vite)
- **Styling**: Vanilla CSS with Tailwind-inspired utilities.
- **Mapping**: Leaflet.js with TopoJSON.
- **Charts**: Recharts & D3.
- **State Management**: Zustand.

---

## 🚦 How to Use
1. **Upload**: Drag and drop your CSV/Excel file into the Data Manager.
2. **Set Columns**: Go to "Column Settings" to ensure your Sales/Values are marked as 'Measures'.
3. **Explore**: Use the Map View to see geographical trends.
4. **Analyze**: Head to the Analytics tab for detailed charts.
5. **Save**: Click the "Save Workspace" button to persist your progress.
