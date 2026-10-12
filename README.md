# India-Stocks-451-480-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 451 to 480)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-451-480-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (451 to 480)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 451 | `SHYAMMETL` | Shyam Metalics and Energy Ltd. | `SHYAMMETL.NS` |
| 452 | `SIGNATURE` | Signatureglobal (India) Ltd. | `SIGNATURE.NS` |
| 453 | `SOBHA` | Sobha Ltd. | `SOBHA.NS` |
| 454 | `SONACOMS` | Sona BLW Precision Forgings Ltd. | `SONACOMS.NS` |
| 455 | `STARHEALTH` | Star Health and Allied Insurance Company Ltd. | `STARHEALTH.NS` |
| 456 | `STLTECH` | Sterlite Technologies Ltd. | `STLTECH.NS` |
| 457 | `SUMICHEM` | Sumitomo Chemical India Ltd. | `SUMICHEM.NS` |
| 458 | `SUNTV` | Sun TV Network Ltd. | `SUNTV.NS` |
| 459 | `SUNDARMFIN` | Sundaram Finance Ltd. | `SUNDARMFIN.NS` |
| 460 | `SWANCORP` | Swan Corp Ltd. | `SWANCORP.NS` |
| 461 | `SYNGENE` | Syngene International Ltd. | `SYNGENE.NS` |
| 462 | `SYRMA` | Syrma SGS Technology Ltd. | `SYRMA.NS` |
| 463 | `TBOTEK` | TBO Tek Ltd. | `TBOTEK.NS` |
| 464 | `TDPOWERSYS` | TD Power Systems Ltd. | `TDPOWERSYS.NS` |
| 465 | `TATACHEM` | Tata Chemicals Ltd. | `TATACHEM.NS` |
| 466 | `TATAELXSI` | Tata Elxsi Ltd. | `TATAELXSI.NS` |
| 467 | `TATAINVEST` | Tata Investment Corporation Ltd. | `TATAINVEST.NS` |
| 468 | `TATATECH` | Tata Technologies Ltd. | `TATATECH.NS` |
| 469 | `TTML` | Tata Teleservices (Maharashtra) Ltd. | `TTML.NS` |
| 470 | `TECHNOE` | Techno Electric & Engineering Company Ltd. | `TECHNOE.NS` |
| 471 | `TEGA` | Tega Industries Ltd. | `TEGA.NS` |
| 472 | `TEJASNET` | Tejas Networks Ltd. | `TEJASNET.NS` |
| 473 | `TENNIND` | Tenneco Clean Air India Ltd. | `TENNIND.NS` |
| 474 | `THANGAMAYL` | Thangamayil Jewellery Ltd. | `THANGAMAYL.NS` |
| 475 | `NIACL` | The New India Assurance Company Ltd. | `NIACL.NS` |
| 476 | `RAMCOCEM` | The Ramco Cements Ltd. | `RAMCOCEM.NS` |
| 477 | `THERMAX` | Thermax Ltd. | `THERMAX.NS` |
| 478 | `TIMKEN` | Timken India Ltd. | `TIMKEN.NS` |
| 479 | `TITAGARH` | Titagarh Rail Systems Ltd. | `TITAGARH.NS` |
| 480 | `TORNTPOWER` | Torrent Power Ltd. | `TORNTPOWER.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream SHYAMMETL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-451-480-Historical-Data/main/SHYAMMETL/1m/2026/10/SHYAMMETL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
