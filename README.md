# Automation Integrity ROI Calculator

A standalone HTML-based ROI calculator for evaluating the business value of Automation Integrity across one or more DCS sites.

## Overview

This tool provides an interactive calculator that lets you adjust engineering effort, labor assumptions, investment costs, efficiency gains, and analysis horizon to estimate:

- Annual savings per DCS
- Multi-year realized benefits
- Total investment
- Net savings
- ROI percentage
- Payback period

The application is implemented as a single HTML file with embedded CSS and JavaScript, so it can be opened directly in a browser without a build step.

## Features

- Clean dashboard UI with live-updating calculations
- Adjustable efficiency gain slider
- Editable labor, effort, and investment assumptions
- Investment schedule table with annual support escalation
- ROI summary, payback timeline, and financial overview
- Multi-site rollup
- Word report export using the `docx` browser library

## Files

- `index.html` — main application
- `wiki-content/` — source markdown used for the GitHub wiki

## How to Use

1. Open `index.html` in a web browser.
2. Adjust the input assumptions in the left panel.
3. Review updated ROI metrics and tables on the right.
4. Click **Download Word Report** to export the current scenario.

## Default Baseline

The default values are configured around the provided ROI worksheet assumptions, including:

- 70% efficiency gain
- $200/hr engineer labor rate
- 251 work days per year
- 2 items researched per day
- 5-year analysis horizon

## Calculation Notes

The calculator derives:

- **Annual Savings** from the difference between current-state and automated annual labor cost
- **Realized Benefits** as annual savings multiplied by analysis years
- **Net Savings** as realized benefits minus total investment
- **ROI** as `(Net Savings / Total Investment) * 100`
- **Payback Period** based on Year 1 investment divided by annual savings

## Recent Fix

The calculator functionality was repaired by fixing a JavaScript syntax error in the Word export section that prevented the full script from loading. The UI and layout were intentionally left unchanged.

## Running Locally

No installation is required.

```text
Open index.html in your browser
```

## License

Internal / project-specific use unless otherwise defined by the repository owner.
