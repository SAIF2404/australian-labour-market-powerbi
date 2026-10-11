# Australian unemployment before COVID (1978–2019)
![Australian unemployment Power BI dashboard](Australian%20unemployment%20Power%20BI%20dashboard.png)

A Power BI case study of how Australia's monthly trend unemployment rate changed before COVID-19. The report is designed as a concise, interactive briefing: a time-series chart shows the long-run pattern, a Year slicer supports focused comparisons, and cards show the latest, peak, and lowest rates for the selected period.

## Key findings

- The pre-COVID rate peaked at **11.11% in November 1992**.
- It reached a low of **4.16% in March 2008**, a decline of **6.95 percentage points** from that peak.
- The rate was **5.16% in December 2019**.

These are descriptive findings. The chart alone does not establish why the rate changed.

## Data and method

Source: Australian Bureau of Statistics (ABS), [Labour Force, Australia](https://www.abs.gov.au/statistics/labour/employment-and-unemployment/labour-force-australia/latest-release), source workbook `62020001.xlsx`. The report uses the **monthly trend unemployment rate for persons**. The report's page filter includes dates before 1 January 2020, so the analysis ends in December 2019.

The source sheet contains metadata above the observations. In Power Query, those first nine metadata rows were removed, the date and unemployment-rate columns were kept, and their types were set for reporting. Rates are displayed as percentages; the difference between two rates is reported in **percentage points**.

The Year slicer filters the chart and KPI cards. The written full-period finding is a static annotation, clearly labelled as covering 1978–2019.

## Files

- `Australian Labour Market.pbix` — interactive Power BI Desktop report.
- `data/62020001.xlsx` — ABS source workbook used by the report.

## Open and refresh

1. Download this repository and open `Australian Labour Market.pbix` in Power BI Desktop.
2. Use the Year slicer to inspect individual years; clear its selection to return to the full pre-COVID view.
3. If Power BI asks for the source workbook when refreshing, use **File → Options and settings → Data source settings → Change Source** and point it to `data/62020001.xlsx` in your downloaded folder.

The supplied workbook may contain later months, but the report's date filter keeps the displayed analysis within the pre-COVID period.
