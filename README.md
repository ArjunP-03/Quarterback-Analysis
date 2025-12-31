# Quarterback Performance Under Fourth-Quarter Pressure (2025)

## Overview
Quarterback performance in high-leverage moments is often discussed narratively as being “clutch” or “not clutch.” This project uses NFL play-by-play data from the 2025 season to evaluate how quarterbacks perform in defined fourth-quarter pressure situations relative to their normal performance earlier in games.

The goal is not to label quarterbacks definitively, but to identify tendencies in efficiency under pressure using Expected Points Added (EPA).

---

## Data
- Source: NFL play-by-play data via `nfl_data_py`
- Season: 2025
- Plays analyzed: Pass plays only
- Minimum threshold: Quarterbacks with 400+ completions

---

## Methodology

### Baseline Performance
- All pass plays in quarters 1–3
- EPA per play calculated for each quarterback

### Fourth-Quarter Pressure Definition
A play is considered a high-pressure situation if:
- It occurs in the 4th quarter
- Score differential is within 7 points
- Down is either:
  - 3rd down with 7+ yards to go, or
  - Any 4th down

### Metric
- **EPA per play** (primary metric)

Quarterbacks are compared based on their baseline EPA (quarters 1–3) versus their EPA in fourth-quarter pressure situations.

---

## Visualizations
The analysis includes:
- Overall EPA distributions
- EPA under pressure (non-4th quarter)
- EPA under pressure (4th quarter)
- Scatter plot comparing baseline EPA to fourth-quarter pressure EPA

In the scatter plot:
- Top-right quadrant indicates strong performance both overall and under late-game pressure
- Points above the diagonal represent quarterbacks who improve in fourth-quarter pressure situations
- Points below the diagonal indicate a decline under late-game pressure

---

## Key Findings
- Quarterbacks vary widely in how their efficiency changes under fourth-quarter pressure.
- Strong baseline EPA does not guarantee strong late-game performance.
- Some quarterbacks improve in high-leverage fourth-quarter situations, while others experience noticeable declines.
- Late-game pressure performance appears more volatile than early-game efficiency.

---

## Limitations
- Game context such as time remaining and timeout availability is not fully captured.
- Roster strength and supporting cast (offensive line, receivers, play-calling) are not considered.
- EPA reflects play outcomes rather than decision quality.
- High-pressure fourth-quarter situations represent smaller sample sizes.
- Results are based on a single season and may not reflect long-term trends.

---

## Reusability
This notebook is designed to be reusable across seasons.  
To analyze a different year, users can modify the `season_year` parameter at the top of the notebook, provided play-by-play data is available for that season.

---

## Future Work
Potential extensions include:
- Incorporating time remaining or win probability
- Adjusting for opponent defensive strength
- Multi-season comparisons to test year-to-year stability
- Incorporating pass-rush pressure data

---

## Tools Used
- Python
- pandas
- matplotlib
- nfl_data_py

---

## Conclusion
This project demonstrates that quarterback performance under pressure is situational and cannot be fully inferred from overall efficiency alone. Evaluating performance across multiple pressure contexts provides a more nuanced understanding of late-game quarterback play.
