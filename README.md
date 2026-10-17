# RingConn Health Coach

Upload the data export from your RingConn Gen 3 ring (`data.zip` or the three CSV files) and get a private analysis of how sleep, heart rate, HRV, SpO2 and activity connect.

- **Runs entirely in your browser.** No backend, no uploads, no tracking. The only external requests are the Google Fonts stylesheet and the JSZip library from cdnjs.
- **Inputs:** `Activity-*.csv`, `Sleep-*.csv`, `Vital Signs-*.csv` (detected automatically, zip subfolders are fine).
- **What you get:** personal baselines, a day timeline, Spearman correlations with n and permutation p-values, rule-based anomaly hints, a coaching plan with one experiment, and app ideas derived from your data.
- **Demo data** on first load is synthetic.

Wellness insights from consumer-ring data, not medical advice.

## Run locally

It is a single static file. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy

Static site, no build step. On Vercel: import the repo with the "Other" framework preset and leave the build command and output directory empty.
