# RingConn Health Coach

Upload the data export from your RingConn Gen 3 ring (`data.zip` or the three CSV files) and get a private analysis of how sleep, heart rate, HRV, SpO2 and activity connect.

- **Runs entirely in your browser.** No backend, no uploads, no tracking. The only external requests are the Google Fonts stylesheet and the JSZip library from cdnjs.
- **Inputs:** `Activity-*.csv`, `Sleep-*.csv`, `Vital Signs-*.csv` (detected automatically, zip subfolders are fine).
- **What you get:** personal baselines with usual-range bands and median lines on every trend (diamonds mark values outside your range in the unfavorable direction), a day timeline with a shared crosshair, Spearman correlations with n and permutation p-values, rolling 7-day SpO2 rule, rule-based anomaly hints, a coaching plan, a before/after experiment tracker, a weekly recap and app ideas derived from your data.
- **Context log:** tap a day to tag caffeine, alcohol, training, symptoms and add a note. Stored only in your browser (localStorage), shown as markers on the timeline.
- **Guardrails:** scatter plots for sleep onset and steps unlock at 14 points, step targets only after 21+ days with a real relationship, partial days are never scored, data-quality chips and P/U/G badges mark gaps.
- **Demo data** on first load is synthetic.

Wellness insights from consumer-ring data, not medical advice.

## Run locally

It is a single static file. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy

Static site, no build step. On Vercel: import the repo with the "Other" framework preset and leave the build command and output directory empty.
