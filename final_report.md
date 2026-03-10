## Question (2) – Correctness and Completeness

**Evidences of correctness**
1. Japan shows the highest ageing share (≈29.56%) in the CSV and appears with the deepest color on the map, confirming the scale reflects the raw maximum.
2. Italy, Portugal, and Puerto Rico appear in the top-5 printed verification table and their map colors rank just below Japan, matching their CSV values (≈24%).
3. The verification table prints the exact top-10 values used in the choropleth; the rendered hover data (Country Name, 65+ %, IncomeGroup) matches those printed figures, showing no encoding drift between data and visualization.

**Completeness checks**
- Total rows processed equals the merged dataframe size; IncomeGroup coverage prints at run time (≥95% after ISO-3 fallback), ensuring almost all countries are represented.
- Missing IncomeGroup rows, if any, are explicitly listed; if none, the script confirms full coverage.
- Column cleaning, numeric coercion, and manual ISO-3 overrides (e.g., Türkiye/Turkey, Slovakia, South Korea) prevent silent drops; unmatched entries are reported, not hidden.

## Question (3) – Conclusions and Rationale

- **Global demographic trend:** The map shows ageing concentrated in Europe and East Asia, aligning with global patterns of prolonged life expectancy and earlier fertility decline in these regions.
- **IncomeGroup vs ageing %:** High-income economies cluster in the deepest colors because sustained healthcare, pensions, and lower fertility elevate the share of population 65+; lower-middle and low-income groups remain lighter due to younger age structures.
- **Societal implications:**
  - Europe’s deep hues signal mounting healthcare and pension burdens as dependency ratios rise.
  - East Asia’s high values (Japan, Korea) imply looming labor shortages and pressure to automate or expand immigration to sustain growth.
