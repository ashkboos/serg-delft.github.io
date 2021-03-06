---
layout: page
title: Large-Scale API misuse Detection
---

#### Background

At the Software Analytics Lab (SAL), we are developing techniques to construct
precise and fine-grained dependency networks of package repositories such as
[Maven](https://mvnrepository.com/) or
[crates.io](https://crates.io) using methods from program analysis. Typically,
we build dependency networks from dependency descriptors in package metadata
files such as `pom.xml`, `package.json` or `Cargo.toml`, yielding an imprecise
representation as it does not account for how and what portion of dependencies
in a single package are _actually_ being used in the source code.  Recently, we
have developed a systematic approach to creating _call-based dependency
networks_ (CDNs) by inferring the dependency use at the function call level of
packages. Such a representation makes it possible for the first time to perform
analysis such as precise security vulnerability tracking, software license
tracking and data-based API evolution studies on a dependency network.  Our
first evaluation of building a CDN for [crates.io](https://crates.io) has shown
promising results and we are now looking for interested master students to
explore new avenues with this work!

#### Problem Statement

A common and prevalent problem is the misuse of APIs [1]. A misuse is a
violation of _usage constraints_ of an API. As an example, this can be to forget
to close an _I/O Stream_ after reading a file when attempting to read a new
file. While tools exist to detect API misuse on a project level, developers are
unaware if they through _transitive_ dependencies make calls to a chain of
underlying APIs that are prone to misuse (e.g., a dependency may forget to close
a file).  The aim of this project is to create an API misuse detector to study
the widespread (e.g., propagation) and implications of API misuse in a package
repository.

#### Related work

[1] Amann, Sven, et al. "A Systematic Evaluation of Static API-Misuse
Detectors." IEEE Transactions on Software Engineering (2018).

[2] J. Hejderup, A. van Deursen, and G. Gousios, “Software Ecosystem Call Graph for
Dependency Management,” in Proceedings of the 40th International Conference on
Software Engineering: New Ideas and Emerging Results, New York, NY, USA, 2018,
pp. 101–104.

#### Contacts about the project:

* [Joseph Hejderup](mailto:j.i.hejderup@tudelft.nl) (TU Delft)
* [Georgios Gousios](mailto:g.gousios@tudelft.nl) (TU Delft)