# Robot Spare Bin: Sales Data Bot

A browser automation bot built as part of the [Robocorp Beginner Course](https://sema4.ai/docs/automation/courses/beginners-course-python). It logs into a demo intranet site, downloads a sales data spreadsheet, fills out the web form for each sales rep, and exports the results as a PDF.

## What it does

1. Opens [robotsparebinindustries.com](https://robotsparebinindustries.com) and logs in
2. Downloads `SalesData.xlsx` (sales rep names, sales figures, and targets)
3. Fills out the sales form for each row in the spreadsheet
4. Screenshots the results summary
5. Exports the results to `output/sales_results.pdf`

## Tech

- [Robocorp](https://robocorp.com) / `rpaframework` — browser automation and PDF/Excel handling
- Playwright-based browser control via `robocorp-browser`

## Running

**Using RCC (recommended — handles environment setup automatically):**
```bash
rcc run
```

**Using an existing conda environment:**
```bash
conda env create -f conda.yaml
conda activate rpaframework
python -m robot --report NONE --outputdir output --logtitle "Task log" tasks.robot
```

Output files land in the `output/` folder.
