## CBDB Surname Summarization

Welcome to the CBDB Surname Summarization project repository. This project provides interactive visual summaries of surname data from the China Biographical Database Project (CBDB). The data is downloaded from the official HuggingFace mirror, surnames are extracted and tallied, and the results are presented in a single-file interactive web page that includes the classic Hundred Family Surnames (《百家姓》) ranking and the non-Hundred Family Surnames table.

## Visualization Items

This repository includes visualizations for the following aspects of the CBDB surname data.

- **Surname Top N Bar Chart.** Explore the distribution of the most common surnames. A slider shows the top 5 to 50 surnames, with wine-red bars, hover tooltips that display the count, the share of persons with recorded surnames, the share of the Top 20, and the Hundred Family Surnames (《百家姓》) rank, plus PNG export.
- **Hundred Family Surnames Rank Table (《百家姓》).** Browse all 504 surnames of the classic text in their original order, with CBDB counts (0 where CBDB has no record).
- **Non-Hundred Family Surnames Table.** List surnames not included in the classic 504, sorted by count in descending order.

## Demonstration

Visit the [CBDB Surname Demonstration](https://sokachcarpediem.github.io/CBDB_Surname/CBDB_Surname.html) to interact with the visualizations.

## Repository Contents

| File | Description |
|---|---|
| `CBDB_Surname.html` | Single-file interactive visualization (HTML/CSS/JS and data all inlined) |
| `template.html` | HTML template (placeholder-based) used to generate the page |
| `cbdb_surname_extraction.ipynb` | Download the CBDB SQLite database and extract raw surnames |
| `build_cbdb_surname_tables.ipynb` | Build the Hundred Family Surnames (《百家姓》) and non-Hundred Family Surnames raw tables (simplified and traditional merging) |
| `build_cbdb_surname_website.ipynb` | Generate the single-file HTML website from the data JSONs |
| `surnames_raw.json` | Raw surname counts, keyed by surname |
| `bjx_raw.json` | Hundred Family Surnames (《百家姓》) 504-rank table as `[surname, count, rank]` |
| `extra_raw.json` | Non-Hundred Family Surnames as `[surname, count]` |

## How to Reproduce

1. Run `cbdb_surname_extraction.ipynb` to download the latest CBDB SQLite and extract `surnames_raw.json`.
2. Run `build_cbdb_surname_tables.ipynb` to generate `bjx_raw.json` and `extra_raw.json`.
3. Run `build_cbdb_surname_website.ipynb` (together with `template.html`) to generate `CBDB_Surname.html`.

## Contributors

[Hanzhang Shan](https://github.com/SokachCarpediem), MSc in Digital Humanities, University College London

## License

This project is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). You are free to use and share the content for non-commercial purposes, as long as you provide appropriate attribution and share any derivative works under the same license.
