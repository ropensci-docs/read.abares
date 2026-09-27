# Get or Set read.abares Options

A convenience function to get or set options used by
[read.abares](https://CRAN.R-project.org/package=read.abares). These are
package-level persistent options.

## Usage

``` r
read.abares_options(...)
```

## Arguments

- ...:

  Named options to set, or no arguments to retrieve current values.

## Value

A list of current option values.

## See also

Other read.abares-options:
[`read.abares-options`](https://docs.ropensci.org/read.abares/reference/read.abares-options.md)

## Examples

``` r
# See currently set options for {read.abares}
read.abares_options()
#> $read.abares.max_tries
#> [1] 3
#> 
#> $read.abares.timeout
#> [1] 5000
#> 
#> $read.abares.timeout_connect
#> [1] 20
#> 
#> $read.abares.user_agent
#> [1] "read.abares R package 3.0.1 https://github.com/ropensci/read.abares"
#> 
#> $read.abares.verbosity
#> [1] "default"
#> 

# Set verbosity to quiet and suppress messages
read.abares_options(read.abares.verbosity = "quiet")
read.abares_options()
#> $read.abares.max_tries
#> [1] 3
#> 
#> $read.abares.timeout
#> [1] 5000
#> 
#> $read.abares.timeout_connect
#> [1] 20
#> 
#> $read.abares.user_agent
#> [1] "read.abares R package 3.0.1 https://github.com/ropensci/read.abares"
#> 
#> $read.abares.verbosity
#> [1] "quiet"
#> 
```
