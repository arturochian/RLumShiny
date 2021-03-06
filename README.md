# RLumShiny

A collection of 'shiny' applications for the R package 'Luminescence'. These mainly, but not exclusively, include applications for plotting chronometric data from e.g. luminescence or radiocarbon dating. It further provides access to bootstraps tooltip and popover functionality and contains the 'jscolor.js' library with a custom 'shiny' output binding.

## Installation

To install the stable version from CRAN, simply run the following from an R console:

```r
install.packages("RLumShiny")
```

To install the latest development builds directly from GitHub, run

```r
if(!require("devtools"))
  install.packages("devtools")
devtools::install_github("tzerk/RLumShiny@master")
```

## Applications

The RLumShiny package provides a single function from which all apps can be started: `app_RLum()`. It essentially only takes one argument, which is a unique keyword to specify which app to start. See the table below for a list of available apps and which keywords to use.

| Application | Keyword | Function |
|-------------|---------|----------|
| Abanico Plot | abanico | `plot_AbanicoPlot` |
| Histogram | histogram | `plot_Histogram` |
| Kernel Density Estimate Plot | KDE | `plot_KDE` |
| Radial Plot | radialplot | `plot_RadialPlot` |
| Dose Recovery Test | doserecovery | `plot_DRTResults` |
| Cosmic Dose Rate | cosmicdose | `calc_CosmicDoseRate`|

The `app_RLum()` function is just a wrapper for `shiny::runApp()`. Via the `...` argument further arguments can be directly passed to `shiny::runApp()`. See `?shiny::runApp` for further details on valid arguments.

## Extending Shiny

In addition to its main purpose of providing convenient access to the Luminescence shiny applications this package also provides further functions to extend the functionality of shiny. From the Bootstrap framework the JavaScript tooltip and popover components can be added to any shiny application via `tooltip()` and `popover()`.

It further provides a custom input binding to the JavaScript/HTML color picker [JSColor](http://jscolor.com). Offering access to most options provided by the JSColor API the function `jscolorInput()` is easily implemented in a shiny app. RGB colors are returned as hex values and be directly used in **R**'s base plotting functions without the need of any format conversion.

## Examples

### Abanico Plot app 

`app_RLum("abanico")`

<img src="http://zerk.canopus.uberspace.de/img/github/abanicoApp.png"></img>

### Tooltip 

`tooltip(refId, text, attr = NULL, animation = TRUE, delay = 100, html = TRUE, placement = "auto", trigger = "hover")`

<img src="http://zerk.canopus.uberspace.de/img/github/tooltip.png"></img>

### JSColor 

`jscolorInput(inputId, label, value, position = "bottom", color = "transparent", mode = "HSV", slider = TRUE, close = FALSE)`

<img src="http://zerk.canopus.uberspace.de/img/github/JSColor.png"></img>

## Contribute

This package is part of the R Luminescence project. The is based on and evolves from ideas, contributions and constructive criticism of its users. Help us to maintain and develop the package, to find bugs and create new functions as well as a user-friendly design. Visit our [message board](https://forum.r-luminescence.de) or write us an [e-mail](mailto:team@r-luminescence.de) if anything crosses your mind or if you want your new self-written shiny application to be to implemented. You are kindly invited to bring forward the package with us!

## Note

This version is a development version and it comes without any guarentee! For stable branches please visit
the package on [CRAN 'RLumShiny'](http://cran.r-project.org/web/packages/RLumShiny/index.html).

## License

The RLumShiny package is licensed under the GPLv3. See these files in the main directory for additional details: 

- LICENSE.note
