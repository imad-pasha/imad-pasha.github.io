+++
image = "maskfill1.png"
date = "2020-01-21"
title = "maskfill"
+++



## A robust and simple method for filling in masked data in astronomical images
Astronomical images often have regions with missing or unwanted information, such as bad pixels,
bad columns, cosmic rays, masked objects, or residuals from imperfect model subtractions. In certain
situations it can be essential, or preferable, to fill in these regions. Most existing methods use low
order interpolations for this task. In this paper a method is described that uses the full information
that is contained in the pixels just outside masked regions. These edge pixels are extrapolated inwards,
using iterative median filtering. This leads to a smoothly varying spatial resolution within the filled-in
regions, and ensures seamless transitions between masked pixels and good pixels. Gaps in continuous,
narrow features can be reconstructed with high fidelity, even if they are large. The method is implemented in maskfill, an open-source MIT licensed Python package.†
Its performance is illustrated
with several examples, and compared to several alternative interpolation schemes.

- Code repo: [https://github.com/dokkum/maskfill](https://github.com/dokkum/maskfill)
- Docs: [https://maskfill.readthedocs.io](https://maskfill.readthedocs.io)
- arXiv: [https://arxiv.org/abs/2312.03064](https://arxiv.org/abs/2312.03064)
- PASP: Accepted! Coming soon. 
