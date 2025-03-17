# Quantum Edge Detection

This repository includes Mathematica code and supplementary files used in our paper *Edge Detection* (https://arxiv.org/abs/2405.11373).

## Description

An in-depth paragraph about your project and overview of use.


Our paper introduces Quantum Edge Detection (QED), a quantum protocol for identifying the boundaries of quantum domains where all particles share the same pure state. Focusing on a one-dimensional string of particles, we develop an optimal QED protocol and efficiently compute its success probability using Schur-Weyl duality and Semidefinite Programming (SDP) techniques. We analyze how the success probability depends on the string length and local dimension, with particular emphasis on the limit of long strings. We also present a protocol based on square root measurement, which we prove to be asymptotically optimal. Additionally, we explore a mixed quantum change point detection scenario, where the particle state transitions from known to unknown—a framework with potential applications in detecting malfunctions in quantum devices.  

SDP is now a standard optimization technique implemented in various platforms, including Python, MATLAB, and Mathematica. Given Eq. (15) and the expressions for the Gram matrix in Eq. (48) (Appendix B), implementing the code to optimize the QED protocol is straightforward, so we do not provide it here.  

However, computing the asymptotic performance of the Square Root Measurement (SRM) protocol—particularly deriving the Taylor series expansion for P(x) in Eq. (53), with coefficients listed in Tables 3–6, is more complex and computationally intensive. This is the focus of this repository. The Mathematica notebook **PertExp.nb** contains the relevant code. The files **PLis_d_ORD.m**, where d is the local dimension and ORD is the highest order of the expansion, each consist of a long list of series expansions in inverse powers of N, the length of the string, obtained using **PLis_d_ORD**. Computing these list is the most time demanding part of the calculation. The interested reader, can modify the value of d and ORD and produce similar files for their choice of these parameters (high values of ORD will result in long execution time).

Celdas posteriores en **PertExp.nb**, permiten leer los ficheros **PLis_d_ORD.m** y calcular a partir de ellos la series de Taylor de P(x) para la dimension local d elegida y su aproximante de Pade diagonal, que es el que ofrece mejores resultados. Los coeficientes de estas series y aproximantes de Pade se almacenan en ficheros de texto debidamente formateados para ser typseteados en Latex: **TaylorTable.txt** y **PadeTable.txt**

For completeness, we also include files with additional expansions.  



## Getting Started

### Dependencies

* Describe any prerequisites, libraries, OS version, etc., needed before installing program.
* ex. Windows 10

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program
* Step-by-step bullets
```
code blocks for commands
```

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. Dominique Pizzie  
ex. [@DomPizzie](https://twitter.com/dompizzie)

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release

## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details

## Acknowledgments

Inspiration, code snippets, etc.
* [awesome-readme](https://github.com/matiassingers/awesome-readme)
* [PurpleBooth](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2)
* [dbader](https://github.com/dbader/readme-template)
* [zenorocha](https://gist.github.com/zenorocha/4526327)
* [fvcproductions](https://gist.github.com/fvcproductions/1bfc2d4aecb01a834b46)
Mathematica code for the paper Quantum Edge Detection https://arxiv.org/abs/2405.11373
