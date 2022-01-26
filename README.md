
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Introduction

<!-- badges: start -->

[![Project Status: Concept – Minimal or no implementation has been done
yet, or the repository is only intended to be a limited example, demo,
or
proof-of-concept.](https://www.repostatus.org/badges/latest/concept.svg)](https://www.repostatus.org/#concept)
[![Last-changedate](https://img.shields.io/badge/last%20change-2021--12--15-yellowgreen.svg)](/commits/master)
<!-- badges: end -->

`rirods` is an integration solution whose aim is to allow users within R
to work efficiently and comfortably with iRODS data objects, following
the R paradigms they are familiar with. Standard R objects are accepted
and returned. Furthermore, the design minimizes dependency on tools
beyond iRODS itself in order to both limit complexity of deployment and
to benefit from the performance optimizations present in the core iRODS.

The `rirods` package has been engineered to have semantics equivalent to
the iCommands and can easily be used as a basis for further
customization.

It was initially developed at the Nestle Institute of Health Sciences by
Radovan Chytracek, Richard Coté, and Bernhard Sonderegger; based
heavily on iCommands code. And is currently being updated for iRODS 4.2+
by Kory Dorrell Draughn, Terrell Russell and Martin Schobben.

## Installation

You can install the development version of `rirods` from GitHub with
`devtools`:

``` r
# Install rirods from GitHub: 
# install.packages("devtools")
devtools::install_github("irods/irods_client_library_r_cpp")
```

## System requirements

To use rirods, a minimal installation of iRODS is required (see the
[manual](https://docs.irods.org/4.2.10/getting_started/installation/)),
and requires Ubuntu 18.04 LTS (Bionic Beaver).

``` bash
apt-get install irods-dev irods-runtime
```

In addition clang6.0.0 is needed for compilation

``` bash
apt-get install clang6.0.0
```

Kerberos is needed for the authenticating of users and services on a
network.

``` bash
apt-get install libkrb5-dev
```

And the Jansson C library for encoding, decoding and manipulating of
JSON data.

``` bash
apt-get install jansson2.7-0
```

## Example

This is a basic example which shows you how to solve a common problem:

    library(rirods)
    ## basic example code
