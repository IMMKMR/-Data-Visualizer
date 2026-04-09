# 📊 Data Visualizer: Professional User Manual
### *Mastering India's Premier Geo-Analytics & BI Platform*

<img width="1915" height="911" alt="image" src="https://github.com/user-attachments/assets/0ecb6f0d-0b1a-405c-8c1c-f7f7a8b2419b" />

This manual provides an **in-depth look** at every feature, configuration, and data rule within the Data Visualizer environment. Designed for high-performance business analysis, this tool transforms raw spreadsheets into a visual command center for India's geographic data.

<img width="1916" height="906" alt="image" src="https://github.com/user-attachments/assets/3a00e9e0-dfa3-4c23-8566-6494095bba6e" />

<img width="1918" height="907" alt="image" src="https://github.com/user-attachments/assets/dd2e1d28-c90d-4ea1-9e2f-c83f4c7adbed" />


## 📂 Section 1: Detailed Spreadsheet Formatting
The foundation of your dashboard is a well-formatted Excel or CSV file. The system uses **Fuzzy Logic Detection** to identify your data, but following these strict rules ensures 100% accuracy.

<img width="882" height="376" alt="image" src="https://github.com/user-attachments/assets/6e63bef3-beb0-4d27-9a77-634a02095d32" />


### 1.1 The "Golden" Cleanliness Rules
*   **Header Row**: Row 1 **must** contain your column titles. Ensure there are no empty rows or "Title Blobs" above your headers.
*   **Data Consistency**: Districts like `Bangalore` and `Bengaluru` are treated as different entities. Use a consistent naming convention.
*   **No Formulas in Headers**: Ensure headers are plain text.
*   **Value Types**: Ensure your `Sales` and `Target` columns contain **only numbers**. Remove thousand-separators (commas) if possible, though the tool can handle them.

### 1.2 Recognized Geographic Keywords
The tool scans for these "Aliases" to map your data to the India Geometry:
*   **Districts (Heatmap Ready)**: `District`, `Dist`, `District Name`, `Place`.
*   **State**: `State`, `State Name`, `St`.
*   **Hierarchy**: `Zone`, `Region`, `Territory`, `Branch`.

### 1.3 Pin & Marker Data (GPS Logic)
To see markers on the map, your row **must** have:
*   `Latitude` (19.0760) and `Longitude` (72.8777).
*   **Marker Types**: If you include a `Type` column, use these keywords for custom icons:
    *   **Channel Partner**: `CP`, `Partner`, `Distributor`, `Dealer`.
    *   **Demo Activities**: `Demo`, `Event`, `Activity`, `Star`.
    *   **HQ**: `HQ`, `Headquarter`, `Branch Office`.

---

## 📈 Section 2: Chart Design Studio (Analytics)
The Analytics Dashboard is a drag-and-drop environment for building custom reports.

### 2.1 Understanding Widgets
Each widget is a "Live View" into your data. You can mix and match different views:
*   **KPI Cards**: Best for "Big Picture" metrics like *Total Revenue* or *Total Count of Districts*.
*   **Bar/Area Charts**: Ideal for comparing performance across **Dimensions** (e.g., Sales by State).
*   **Pie/Donut Charts**: Perfect for seeing the "Share of Business" across your Zones or Product categories.

### 2.2 The Configuration Panel (Gear Icon ⚙️)
When you configure a widget, you control the "Data Model":
*   **Group By**: This is your "Slice." If you select `State`, the chart will show one bar for every state.
*   **Metric**: Choose from `Sales`, `Target`, or `Sales + Target`. The **Combined View** overlay lines help you see instantly where you are hitting or missing goals.
*   **Data Source**: If your Excel has multiple sheets (e.g., "Jan Sales", "Feb Sales"), you can select which sheet this specific chart should pull from.

### 2.3 Layout Control
*   **Drag-to-Move**: Click and hold the header of any widget to move it.
*   **Corner Resize**: Grab the dotted corner at the bottom-right to change height and width. The layout is saved **instantly**.

<img width="1919" height="909" alt="image" src="https://github.com/user-attachments/assets/4e0d2188-5261-424f-a172-86576ead09a0" />

## 🗺️ Section 3: Map Intelligence & Interaction
The India Map is interactive and dynamic.

### 3.1 Heatmap Scaling
The colors flow from **Red (Low)** to **Green (High)**.
*   **How it's calculated**: The map identifies the highest Sales figure in your dataset and sets that as 100% (Dark Green). All other districts are shaded proportionally.
*   **Achievement Mode**: If your data has an `Achievement%` column, the map can shade based on your % of target instead of raw sales.

### 3.2 Sidebar Panels (The Control Center)
*   📁 **Projects**: Manage multiple datasets. Switching projects reloads the entire environment.
*   ⬆️ **Upload**: The entry point. Drop files here to start.
*   📊 **Records**: A built-in spreadsheet editor. **Double-click any cell** to fix a typo. Click the Trash icon to remove bad data.
*   ⚙️ **Data Model**: This is for power users.
    *   **Rename Columns**: Change how headers appear in charts without editing your Excel.
    *   **Column Roles**: Manually set a column as a "Dimension" (Text) or a "Measure" (Value).
*   🎛️ **Filters**: Narrow down your view. Selecting "North Zone" will filter both the Map and your Charts simultaneously.

<img width="247" height="138" alt="image" src="https://github.com/user-attachments/assets/f59ad093-b21e-43cd-bd17-19684e2b3c3c" />


## 💾 Section 4: Data Security & Persistence
*   **Zero Server Risk**: Your files are **never** uploaded to a cloud server. All processing happens in your browser's RAM.
*   **The Auto-Sync Engine**: The tool uses a "Local-First" architecture. Every time you move a chart or update a record, it is saved to a secure local database in your browser.
*   **Persistence**: If you close the window and come back tomorrow, the app will remember your exactly where you left off.

## 💡 Section 5: Common Explanations & Troubleshooting

### Why is my Map blank after uploading?
*   **Header Mismatch**: The most common reason is that your "District" column isn't named correctly. Ensure it is named exactly `District`, `District Name`, or `Dist`.
*   **Case Sensitivity**: While the tool is smart, ensure your district names aren't in all-caps or all-lowercase unless necessary (e.g., Use `Mumbai`, not `MUMBAI`).

### How do I switch between different months of data?
*   **Multi-Sheet Excel**: If you upload an Excel file with tabs like "Jan," "Feb," and "Mar," you can switch between them in any chart's **Configure (⚙️)** panel. The map will always display the data from the first sheet by default, but you can update it in the **Manage Records** tab.

### Where is my data saved?
*   **Local Storage**: Your data is stored in your browser's "IndexedDB"—a secure, private vault on your hard drive. It is **not** on a server, which means nobody else can see it.
*   **Clearing Data**: If you want to delete everything, go to the **Projects** tab and delete your workspace.

### Can I use my own colors?
*   **Hex Codes**: Yes! In the chart properties, check the "Custom Color" box. You can enter codes like `#FF5733` for your specific brand color.

<img width="226" height="868" alt="image" src="https://github.com/user-attachments/assets/de5ed0b8-826d-4a89-a3a1-7f5e61f554a7" />

*This dashboard is designed to scale with your business intelligence needs. For high-impact reporting, ensure your geographic data is clean and your metrics are numeric.*

