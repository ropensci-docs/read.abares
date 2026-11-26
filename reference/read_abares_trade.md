# Read Data from the ABARES Trade Dashboard

Fetches and imports ABARES trade data. As the data, `x`, is large,
~1.5GB uncompressed CSV, downloads may be slow. The final object is
sorted by "Fiscal_year" and "Month".

## Usage

``` r
read_abares_trade(x = NULL, code_description = FALSE)
```

## Source

<https://daff.ent.sirsidynix.net.au/client/en_AU/search/asset/1033841/0>

## Arguments

- x:

  A file path providing the file with the data to be imported. The file
  is assumed to be unarchived (*i.e.*, still zipped). This function does
  not provide any checking whether this function is the proper function
  for the provided file. Defaults to `NULL`, assuming that the file will
  be downloaded in the active R session.

- code_description:

  Boolean. Include the trade code description, this results in a larger
  object with long text descriptions for each trade code, and the unit
  of quantity measure, *e.g.*, "KG" (kilograms), "NO" (number/count),
  "L" (litres).

## Value

A [data.table](https://CRAN.R-project.org/package=data.table) object of
the ABARES trade data with the "Trade_code" field as the key for fast
subsetting.

## Note

Columns are renamed for consistency with other ABARES products serviced
in this package using a snake_case format and ordered consistently.
"State" reflects the state of origin of the exported goods, not the
state in which the port of departure is located; it is therefore
expected that "State" and "Australian_port" will not always correspond
geographically.

## References

<https://www.agriculture.gov.au/abares/research-topics/trade/dashboard>

## See also

Other Trade:
[`read_abares_trade_regions()`](https://docs.ropensci.org/read.abares/reference/read_abares_trade_regions.md)

## Examples

``` r
if (FALSE) { # interactive()
trade <- read_abares_trade()

trade

trade_codes <- read_abares_trade(code_description = TRUE)

trade_codes
}
```
