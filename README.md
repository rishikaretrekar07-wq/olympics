# Global Olympic Sports Performance Analysis

A Tableau portfolio project using the supplied Olympic dataset. The detailed athlete-event analysis is filtered to Olympic editions from 1992–2022, matching the assignment's requested start period as interpreted from the screenshot (1992, not 1922). A separate recent-edition medal-table supplement covers selected leading NOCs for 2024 Summer and 2026 Winter.

## Project files
- `data/olympic_results_1992_2022.csv` — detailed athlete-event rows filtered to 1992–2022 (recommended main Tableau data source).
- `data/olympic_results_clean.csv` — original full historical source table (1896–2022), retained for reference.
- `data/athlete_bios_clean.csv` — athlete biographies; join on `athlete_id`.
- `data/medals_by_country.csv` — country/NOC summary.
- `data/medals_by_year_and_games_type.csv` — medal records by year and Summer/Winter type.
- `data/medals_by_discipline.csv` — medal records by discipline.
- `data/country_medal_trends_1992_2022.csv` — country medal trends for 1992–2022.
- `data/medals_by_year_and_games_type_1992_2022.csv` — medal records by year and Games type for 1992–2022.
- `data/participation_by_year_1992_2022.csv` — participation summaries for 1992–2022.
- `data/recent_games_medal_table_supplement_2024_2026.csv` — selected top NOCs from 2024 Summer and 2026 Winter official medal tables; this is a medal-table supplement, not athlete-level event data.
- `data/participation_by_year.csv` — participation and event-result row summaries.
- `Global_Olympic_Analysis_Data.xlsx` — workbook with source tables, summaries, and data dictionary.
- `tableau/Tableau_Build_Guide.md` — calculated fields and dashboard construction plan.
- `documentation/Project_Report_Template.md` — report template for your final findings.

## Dataset scope and limitations
- The uploaded athlete-event source spans 1896–2022. For the main analysis use 1992–2022. The separate 2024/2026 supplement contains only selected leading NOCs' medal-table totals, not detailed athlete-event records, so do not blend it into athlete-level charts.
- 308,408 event-result rows and 145,500 athlete biography rows are included.
- 44,139 result rows contain a Gold, Silver, or Bronze value.
- 2,601 result rows have missing Games type and 2,601 have missing year.
- Team events can list each athlete separately. Therefore, summary values labelled **athlete-medal records** count athlete-event medal records, not unique official medals awarded. Use this definition in chart titles and report text.
- Country/NOC values are source identifiers and should not automatically be treated as current geopolitical country names.
- This dataset does not contain sports investment/funding amounts. Do not claim to analyze investment versus medal outcomes unless a separate, reliable funding dataset is added.
- The 2024 supplement lists the top 10 NOCs only; the 2026 supplement lists the top 15 NOCs only. Sources: Paris 2024 medal table as summarized by the `olympicAthletes` dataset documentation and CONI's Milano Cortina 2026 final medal table (https://www.coni.it/en/italia-team/medals-milano-cortina-2026.html).
- No detailed athlete-event data for 2024 or 2026 is included in the uploaded source. Do not represent the supplement as a complete all-NOC medal table.
- No Tableau `.twb` / `.twbx` file is generated automatically here. Use the build guide to create and save the workbook in Tableau Public or Tableau Desktop.

## Suggested project question
How have Olympic medal records and participation patterns changed across years, countries/NOCs, disciplines, and Summer versus Winter Games?

## Starter observation
Top five NOCs by athlete-medal records in this dataset:
- USA: 5,995 athlete-medal records
- URS: 2,480 athlete-medal records
- GER: 2,399 athlete-medal records
- GBR: 2,199 athlete-medal records
- FRA: 2,009 athlete-medal records

These are athlete-medal records, so team-event participants may contribute multiple rows. Validate the definition before comparing with official medal tables.
