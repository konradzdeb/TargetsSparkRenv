Sample Targets / Spark / renv project
================

## TDL;DR

This repo provides a skeleton project structure that can be quickly
utilised to create an analytical project reflecting configuration using
`renv`, `targets` and Spark, which is handled via `sparklyr` package.

### Rationale

`renv` provides a powerful mechanism for robust dependency management
across R projects. R offers excellent dependency fragment systems
through its package development mechanism. Whereas R package
architecture is suitable for delivery of components that are expected to
be re-used and recycled across other projects it may be unnecessarily
complex for simpler projects that do not have a requirement to be run
frequently. `renv` excellently bridges that gap by offering robust
dependency management that is perfect for standalone analytical
projects. `targets` is another great idea that offers intelligent way of
creating analytical production pipelines that can be tweaked and
enhanced ad infinitum for the purpose of generating updates and results.

Levering those two excellent architectures in a business settings, can
be challenging due to the following perspective:

-   Both concepts require certain amount of configuration. A substantial
    effort by package authors and community was made to create help with
    that challenge; nevertheless, at the moment of writing this document
    this wasn’t fully automated
-   In a business settings, majority of analytical and reporting
    projects will be done against some database / computing backend. In
    the context of this project I’ve utilised Spark
-   The utilised `targets` configuration should be conducive to
    supporting multiple framework. A common scenario in the course of
    exploratory / modelling analysis is to produce analytical materials
    and then subsequently update those following discussions / requests
    for clarification or emerging new interests
-   Artefact generation should be conducive to reusability. In a common
    scenario we would intend to generate a key reporting outputs but
    also make the relevant tables / charts available independently so
    those can be conveniently shared

The repo address those points by providing an *opinioned* set of
settings, which hopefully, make it easy for analysts to incorporate in
their work and develop further in a manner suitable for analysis.
