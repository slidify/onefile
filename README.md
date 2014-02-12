Standalone HTML with Slidify
=======

This repo is a demo showcasing my attempts to allow standalone HTMLs to be created using Slidify. The modifications I have made to Slidify to support this feature reside in the `onefile` branch and so you will need to install it first.

```S
devtools:::install_github('ramnathv/slidify@onefile')
```

This also requires changes to `slidifyLibraries`. However, I decided not to tamper with it for now, and instead modified a few libraries locally, which are all included with this repo.

## How to Test

If you are interested in helping me test this, here is what you need to do

1. Download/Clone this repo.
2. Install the `onefile` branch of slidify.
3. Add slides to `index.Rmd` and Slidify.

I have included an NVD3 plot in this presentation. You can check out other rCharts libraries, say `MorrisJS`. To do this, you will have to do two things

1. In the YAML front matter, do `ext_widgets: {rCharts: [libraries/nvd3, libraries/morris]}`
2. Make sure you are using `myplot$show('inline')` in your `knitr` code chunk.

## Notes

This feature is still very raw and so I would use it with caution. Make sure to read the [advantages and disadvantages of using DataURIs](http://dataurl.net/#advantages).
