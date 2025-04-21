# CO2 Emissions by Vehicle – Power BI Project

This repository contains a Power BI solution for analyzing CO2 emissions by different vehicle types. The project is organized into two main components: the **Semantic Model** (dataset) and the **Report** (visualizations).

## Project Structure

- [`CO2-emissions-by-vehicle.SemanticModel`](CO2-emissions-by-vehicle.SemanticModel/)
  - Contains the Power BI semantic model, including table definitions, data model, and data import logic.
  - Key files:
    - [`definition/model.tmdl`](CO2-emissions-by-vehicle.SemanticModel/definition/model.tmdl): Main model definition.
    - [`definition/tables/Vehicles.tmdl`](CO2-emissions-by-vehicle.SemanticModel/definition/tables/Vehicles.tmdl): Vehicle data table, including calculated columns and data import steps.
    - [`definition/tables/DateTableTemplate_*.tmdl`](CO2-emissions-by-vehicle.SemanticModel/definition/tables/DateTableTemplate_b4b42a47-ea6b-4367-aa90-60bb830d21ba.tmdl): Date table for time-based analysis.
    - [`diagramLayout.json`](CO2-emissions-by-vehicle.SemanticModel/diagramLayout.json): Diagram layout for the data model.

- [`CO2-emissions-by-vehicle.Report`](CO2-emissions-by-vehicle.Report/)
  - Contains the Power BI report definition and resources.
  - Key files:
    - [`report.json`](CO2-emissions-by-vehicle.Report/report.json): Report layout, pages, and visualizations.
    - [`definition.pbir`](CO2-emissions-by-vehicle.Report/definition.pbir): Links the report to the semantic model.
    - [`StaticResources/SharedResources/`](CO2-emissions-by-vehicle.Report/StaticResources/SharedResources/): Custom and built-in themes for report styling.

## Data Source

The dataset is imported from a CSV file:
```
C:\Adventure Works\CO2 emissions by vehicle.csv
```
The import and transformation steps are defined in [`Vehicles.tmdl`](CO2-emissions-by-vehicle.SemanticModel/definition/tables/Vehicles.tmdl).

## Key Features

- **Data Model:** Includes vehicle attributes such as engine size, fuel type, powertrain, transmission, and CO2 emissions.
- **Calculated Columns:** Binned engine sizes for grouped analysis.
- **Visualizations:** 
  - Clustered bar charts, donut charts, scatter plots, decomposition trees, and KPI cards.
  - Pages for different analytical perspectives (e.g., by fuel type, powertrain, engine size).
- **Themes:** Accessible and visually appealing themes for better readability.

## How to Use

1. **Open in Power BI Desktop:**
   - Open the `.pbip` project using Power BI Desktop (with PBIP support).
   - Ensure the data source CSV is available at the specified path or update the path in the model.

2. **Explore the Report:**
   - Navigate through the report pages to analyze CO2 emissions by various vehicle characteristics.

3. **Customize:**
   - Modify the semantic model or report visuals as needed for your analysis.

## Requirements

- Power BI Desktop (latest version recommended)
- Access to the source CSV file: `CO2 emissions by vehicle.csv`

## License

This project is for educational and analytical purposes. Please ensure you have the right to use the underlying data.

---

*For questions or contributions, please open an issue or pull request.*