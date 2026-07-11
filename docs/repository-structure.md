# Repository Structure

The repository is organized around the Microsoft Power BI Project (PBIP) format, which separates the report definitions from the semantic model, making it source-control friendly.

## Root Directories and Files
- `UPI-Transaction-Intelligence-Platform.pbip`: The main Power BI Project file that links the Report and Semantic Model components together. Open this file with Power BI Desktop.
- `UPI-Transaction-Intelligence-Platform.Report/`: Contains the visual layout, pages, and UI definitions of the dashboard stored in PBIR format.
- `UPI-Transaction-Intelligence-Platform.SemanticModel/`: Contains the data model, including table definitions, calculated columns, and Power Query (M) scripts stored in TMDL format.
- `assets/`: Contains screenshots and visual assets for documentation.
- `docs/`: Detailed project documentation (overview, features, data model, etc.).
- `.gitignore`: Configured to ignore Power BI cache files, temporary local settings, and OS-generated files.

## Note on Power BI Generated Files
Files within the `.Report` and `.SemanticModel` directories (such as `.pbir`, `.tmdl`, and internal `.json` files) are generated and managed by Power BI Desktop. While they are text-based and trackable by Git, it is recommended to edit them using the Power BI Desktop application rather than manually modifying them in a text editor to prevent corruption.
