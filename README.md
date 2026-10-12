# Conflict Intensity and Global Search Attention: Evidence from the Russia–Ukraine War

**Marc Boustany & Ahmet Gündüz** · HEC Lausanne, Macroeconometrics · May 2026

📄 [Read the paper (PDF)](paper/ConflictAttention_Boustany_Gunduz.pdf)

## Summary

Do weekly changes in Russia–Ukraine conflict intensity predict worldwide Google search attention for "ukraine war"? Using 171 weekly observations (January 2023 to March 2026), we find a significant one-week transmission from conflict to attention, driven entirely by attacks on **Russian** territory. A one-standard-deviation Russia-territory shock raises attention by 0.49 SD, about three times the Ukraine-territory response. The asymmetry holds in both pro-Ukraine and pro-Russia audiences, and extends to financial markets: Russia-territory attacks Granger-cause changes in the VIX (p = 0.016), while Ukraine-territory attacks do not (p = 0.698). We interpret this as *information normalisation*: combat in Ukraine has become the expected baseline, while attacks on Russian soil remain surprising.

## Methods

- Stationarity analysis (ADF, KPSS), first differences and standardisation
- Autoregressive distributed lag (ADL) models selected by AIC/BIC, with Newey–West (HAC) standard errors
- Impulse response functions with residual-bootstrap confidence bands; ARMA-X robustness check
- VAR and Granger causality tests
- Extensions: audience heterogeneity (pro-Ukraine vs pro-Russia countries) and financial markets (VIX, S&P 500)

## Data

| Source | Content | In this repository |
|---|---|---|
| [ACLED](https://acleddata.com) | Weekly violent events in Ukraine and Russia | No (licence); see [`Data/ACLED/README.md`](Data/ACLED/README.md) |
| [Google Trends](https://trends.google.com) | Weekly search index for "ukraine war", worldwide and by country | Yes, `Data/Google Trends/` |
| FRED / Yahoo Finance | VIX and S&P 500 | Downloaded automatically by the script |

## Reproducing the results

1. Clone or download this repository.
2. Download the ACLED file as described in `Data/ACLED/README.md` and place it in `Data/ACLED/`.
3. Open `Scripts/conflict_attention.Rmd` in RStudio and click **Knit**. Missing R packages (including the `AEC` course package from GitHub) are installed automatically; an internet connection is required.

## Repository structure

```
paper/                    Final paper (PDF)
Scripts/                  R Markdown script (full analysis)
Data/ACLED/               Instructions to download ACLED data
Data/Google Trends/       Google Trends series (worldwide, pro-Ukraine, pro-Russia)
```
