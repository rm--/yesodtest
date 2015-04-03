# Testing the Yesod Web Framework

## some notes to install and run yesod

* run script from [this gist](https://gist.github.com/timmytofu/7417408) to remove all installed packages (that's very useful because there are often problems with global package dependencies, so it's recommended to install all packages in a sandbox)

`ghc-pkg-reset`

* create dir and enter it

`mkdir yesodtest && cd yesodtest` 

* create a directory based sandbox to install packages related to this dir

`cabal sandbox init`

* get latest Haskell packages list

`cabal update`

* install necessary packages

`cabal install alex happy yesod-bin`

* initalize/scaffold Yesod project

`yesod init --bare`

* run tests

`cabal install --run-tests`

* start yesod dev server

`yesod devel`
