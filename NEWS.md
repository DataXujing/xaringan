# CHANGES IN xaringan VERSION 0.2

## NEW FEATURES

- A class `title-slide` was added to the automatically generated title slide (`moon_reader(seal = TRUE)`) so that you can customize the this slide using CSS (thanks, @ekstroem, #7).

- Added an argument `cast_from` to `infinite_moon_reader()` to specify the root directory of the server. Previously the root directory is the directory of the Rmd input file, which makes it impossible for the Rmd document to use resources in upper-level directories (e.g. `![](../gif/cute-kittens.gif)`). Now you can set the working directory to the upper-level directory and call `inf_mr('relative/path/to/input.Rmd')`, so that `input.Rmd` can use any files under the current working directory `./` (thanks, @pat-s, #29).

- Added a Wiki on Github thanks to @pat-s for those who are new to CSS: https://github.com/yihui/xaringan/wiki

## BUG FIXES

- A local copy of MathJax should work with `moon_reader()` (thanks, @bnicenboim, #13).

- Skip fenced code blocks when detecting LaTeX math expressions, e.g. `$api$` in R code `session$api$plot <- ...` should not be treated as a math expression (thanks, @jcheng5).

- Unicode characters can be rendered correctly on Windows now (thanks, @Lchiffon, #20).

# CHANGES IN xaringan VERSION 0.1

## NEW FEATURES

- Initial CRAN release. See the documentation at https://slides.yihui.name/xaringan/
