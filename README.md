# RGlasso.jl
A simple Julia wrapper around the R version of the glasso package. This is not designed to be fast, in particular it uses files not Rif to communicate with R (wich must be on the path).

## Sample usage

This assumes that the `R` executable is available on the path and that the `glasso` package is installed in `R`.

```julia
using RGlasso

data = randn(10,100)
S = cor(data)
rho = 0.01
sparseSInv = glasso(S, rho)
```
