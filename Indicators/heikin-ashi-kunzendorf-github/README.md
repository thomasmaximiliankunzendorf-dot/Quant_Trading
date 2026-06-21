# Heikin Ashi Kunzendorf Indicator

A custom cTrader/cAlgo indicator based on a modified smoothed Heikin Ashi workflow with Bollinger Band overlays.

This repository contains the exportable `.algo` package and extracted metadata for documentation purposes.

## Project status

The uploaded `.algo` file is a compiled cTrader indicator package. The package metadata reports `SourceIncluded: false`, so the original C# source code is not available inside this export. For this reason, the repository keeps the installable `.algo` file in `dist/` and documents the public indicator settings in `docs/`.

## Repository structure

```text
dist/
  Heikin_Ashi_Kunzendorf.algo     # Installable cTrader indicator package

docs/
  algo_metadata.json              # Extracted indicator metadata

src/
  README.md                       # Notes about source-code availability
```

## Indicator overview

- **Name:** ModifiedSmoothedHeikinAshi
- **Type:** cTrader Indicator
- **Overlay:** Yes
- **Time zone:** UTC
- **Target framework:** .NET 6.0

## Output lines

| Line | Property | Plot type | Color |
|---|---|---|---|
| Upper BB | `UpperBB` | Line | #800001FF |
| Lower BB | `LowerBB` | Line | #005727FF |
| Basis | `Basis` | Line | #FFD700FF |
| Upper HA | `UpperHA` | Line | #00BFFFFF |
| Lower HA | `LowerHA` | Line | #FF69B4FF |

## Parameters

| Setting | Property | Type | Default | Group |
|---|---|---|---|---|
| Period | `Period` | Integer | `10` | HA Setting |
| BB Length | `BBLength` | Integer | `20` | HA BB Setting |
| BB StdDev | `BBStdDev` | Double | `2.0` | HA BB Setting |
| BB MaType | `MaType` | Enum | `0` | HA BB Setting |
| Opacity | `Style` | Enum | `1` | Style Setting |
| Opacity | `Opacity` | Integer | `150` | Candle Setting |
| Size | `Size` | Integer | `5` | Candle Setting |
| Up Color | `UpColor` | Color | `#00BFFFFF` | Candle Setting |
| Down Color | `DownColor` | Color | `#FF69B4FF` | Candle Setting |
| Indecisive Color | `IndecisiveColor` | Color | `#800080FF` | Candle Setting |
| Indecisive Threshold (%) | `IndecisiveThreshold` | Double | `10.0` | Candle Setting |

## Installation

1. Open cTrader.
2. Go to **Automate**.
3. Import the file from `dist/Heikin_Ashi_Kunzendorf.algo`.
4. Attach the indicator to a chart and adjust the parameters as needed.

## Notes

This indicator is provided as a technical portfolio project. It is not financial advice and does not guarantee trading performance. Any trading-related use should be tested carefully in demo mode before live use.
