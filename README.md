# Bayesian Data Analysis and Markov Chain Monte Carlo

Tools and code for Bayesian data analysis and Markov chain Monte Carlo workshops.

1. [R programming language](https://www.r-project.org/) and [RStudio](https://www.rstudio.com/)
2. [JAGS (Just Another Gibbs Sampler)](http://mcmc-jags.sourceforge.net/)
3. [Stan](http://mc-stan.org/)

### Installation instructions
All stuff should be portable i.e. working on Linux, Mac and Windows, however we only test it on Windows.

#### R and RStudio
To install R follow [download R](http://cran.r-project.org/mirrors.html) link, choose your mirror and install the latest version.

RStudio is great IDE for R and can be directly download from link [Download RStudio Desktop](http://www.rstudio.com/products/rstudio/download/)

[Resources to learn R](https://github.com/qinwf/awesome-R?utm_campaign=Data%2BElixir&utm_medium=web&utm_source=Data_Elixir_33#resources).

If you do not know where to start [An Introduction to R](https://cran.r-project.org/doc/manuals/r-release/R-intro.html) is quite good.

#### JAGS
[JAGS for Windows](https://sourceforge.net/projects/mcmc-jags/files/JAGS/4.x/Windows/)
To install **rjags** package *RStudio -> Tools -> Install Packages...* and type *'rjags'*

To check it works run this commands in console and there should be no errors
```R
library(rjags)
data(LINE)
LINE$recompile()
LINE.samples <- jags.samples(LINE, c("alpha","beta","sigma"), n.iter=1000)
LINE.samples
```

#### Stan
[RStan Getting Started](https://github.com/stan-dev/rstan/wiki/RStan-Getting-Started) which contains installation instructions.

The main thing for Widnows is installing *toolchain* [Install Rtools for Windows](https://github.com/stan-dev/rstan/wiki/Install-Rtools-for-Windows) and adding them to *PATH* during that installation.
I did not do *configuration* step and test worked.


Relations between R, JUGS and Stan

![alt tag](https://cloud.githubusercontent.com/assets/12628257/16615443/09e052bc-4377-11e6-8ac0-1b7538f757d9.png)
