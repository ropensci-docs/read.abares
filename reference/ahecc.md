# AHECC Classification Codes

Australian Harmonized Export Commodity Classification (AHECC) codes and
their descriptions, sourced from the Australian Bureau of Statistics
(ABS). The classification is based on the January 2022 version of the
AHECC at the 8-digit level.

## Usage

``` r
ahecc
```

## Format

A `data.table` with three columns:

- Trade_code:

  8-digit AHECC export statistical item code (factor).

- uq:

  Unit of quantity used in export documentation, e.g. `KG`, `NO`, `L`.

- Description:

  Plain-text commodity description with parent context applied to
  "Other" categories.

## Source

<https://www.abs.gov.au/statistics/classifications/australian-harmonized-export-commodity-classification-ahecc/latest-release>
