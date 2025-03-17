# Quantum Edge Detection (QED)

This repository contains code and supplementary files related to our paper:  
**Quantum Edge Detection (QED)** – [arXiv:2405.11373](https://arxiv.org/abs/2405.11373)  

## Overview

Our paper introduces **Quantum Edge Detection (QED)**, a quantum protocol for identifying the boundaries of quantum domains where all particles share the same pure state.  

- We focus on a **1D string of particles** and develop an **optimal QED protocol**.  
- The **success probability** is computed using **Schur-Weyl duality** and **Semidefinite Programming (SDP)** techniques.  
- We analyze how the success probability depends on **string length** and **local dimension**, emphasizing the limit of long strings.  
- We present a **Square Root Measurement (SRM) protocol**, proving it to be **asymptotically optimal**.  
- We explore a **mixed quantum change point detection** scenario where the particle state transitions from **known to unknown**, with potential applications in **quantum device diagnostics**.  

## Code and Implementation  

SDP is a **standard optimization technique** implemented in various platforms, including **Python, MATLAB, and Mathematica**. Given Eq. (15) and the Gram matrix expressions in Eq. (48) (Appendix B), implementing the code to optimize the QED protocol is straightforward and **not included in this repository**.  

However, computing the **asymptotic performance** of the **SRM protocol**—specifically, deriving the **Taylor series expansion** for *P(x)* (Eq. 53) with coefficients listed in **Tables 3–6**—is computationally intensive.  

This repository provides the necessary code, primarily in **Mathematica**, to handle these calculations.  

## Files Included  

- **`PertExp.nb`** – Mathematica notebook containing the core calculations.  
- **`PLis_d_ORD.m`** – Precomputed lists of series expansions in inverse powers of *N*, where:  
  - *d* = local dimension  
  - *ORD* = highest order of expansion  
  - Users can modify *d* and *ORD* to generate custom files (*note: higher ORD increases execution time*).  
- **`TaylorTable.txt`** – Formatted coefficients for the **Taylor series** of *P(x)*.  
- **`PadeTable.txt`** – Formatted coefficients for the **Padé approximant**, which provides the most accurate results.  

## Usage  

1. Open **`PertExp.nb`** in Mathematica.  
2. Run the relevant cells to:  
   - Read **`PLis_d_ORD.m`** files.  
   - Compute the **Taylor series** of *P(x)* for a given **local dimension (d)**.  
   - Compute its **diagonal Padé approximant** for improved accuracy.  
3. The resulting coefficients will be saved in **`TaylorTable.txt`** and **`PadeTable.txt`**, properly formatted for LaTeX.  

## Citation  

If you find this repository useful, please consider citing our paper:  
**Quantum Edge Detection (QED)** – [arXiv:2405.11373](https://arxiv.org/abs/2405.11373)  

---

This version improves structure, clarity, and Markdown formatting for GitHub readability. Let me know if you'd like any refinements! 🚀
