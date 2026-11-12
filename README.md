# EmergIntel
**European Emerging Technology Monitor**

EmergIntel is a data analysis project exploring emerging-technology procurement across Europe using public procurement notices published through [Tenders Electronic Daily (TED)](https://ted.europa.eu/).

The project combines XML data processing, structured storage, rule-based classification and interactive analytics to examine procurement activity across technology domains, countries and public-sector buyers.

## Technical workflow

- **Data acquisition:** Downloading and processing TED XML notices.
- **Data engineering:** XML parsing, validation, deduplication and storage in SQLite.
- **Classification:** CPV-based scope filtering and keyword-based technology classification.
- **AI-assisted taxonomy development:** Qwen 2.5 3B was applied to a selected sample of TED procurement notices to identify technology themes and help refine the classification vocabulary.
- **Analytics:** Preparing classified procurement data for exploration in a Streamlit dashboard.

The workflow is organised into separate processing stages and is not yet fully automated.

## Analytical application

The dashboard explores 2024–2025 procurement records through:

- Technology-category and activity trends
- Country and public-buyer comparisons
- Notice and award analysis
- Interactive filters and geographic views

## Methodology

EmergIntel uses a project-defined technology taxonomy combining CPV codes and keyword rules. AI-assisted analysis informed taxonomy development; the dashboard applies the resulting deterministic classification rules.

Notices and awards are treated as separate record types. Category assignments may overlap, so category totals should not be interpreted as mutually exclusive.

The data represents **public procurement signals**, not confirmed technology deployment, expenditure across the entire market or supplier market share. Geographic analysis refers to the recorded location of the contracting authority.

## Technology stack

Python · SQLite · Pandas · Streamlit · Plotly · XML processing · Qwen 2.5 3B

**Data source:** Tenders Electronic Daily (TED), the EU's public procurement notices platform.
