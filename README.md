# Graphs diffusion

## Optimizing Graph Learning using Diffusion

In these experiments I compare different diffusion kernels for Graph diffusion Convolution

Original paper: Diffusion Improves Graph Learning by Klicpera et al.

### Setup:
python==3.8
cuda==11.1
torch==1.8.1

### Used kernels:

#### List of measures:
* Adjacency matrix based kernels:
  * **Katz**: Katz kernel (a.k.a. Walk, Von Neumann diffusion kernel)
  * **Comm**: Communicability kernel (a.k.a. Exponential diffusion kernel)
  * **DFS**: Double Factorial similarity
* Laplacian based kernels:
  * **For**: Forest kernel (a.k.a. Regularized Laplacian kernel)
  * **Heat**: Heat kernel (a.k.a. Laplacian exponential diffusion kernel)
  * **NHeat**: Normalized Heat kernel
  * **Abs**: Absorption kernel
* Markov matrix based kernels and measures:
  * **PPR**: Personalized PageRank
  * **MPPR**: Modified Personalized PageRank
  * **HPR**: PageRank heat similarity measure
* Sigmoid Commute Time:
  * **SCT**: Sigmoid Commute Time
  * **CCT**: Corrected Commute Time
  * **SCCT**: Sigmoid Corrected Commute Time

### References:
* https://papers.nips.cc/paper/2019/file/23c894276a2c5a16470e6a31f4618d73-Paper.pdf 
* https://www.sciencedirect.com/science/article/pii/S0893608012000822 
* https://github.com/klicperajo/gdc
* https://github.com/vlivashkin/pygkernels

### Results

![Cora](https://user-images.githubusercontent.com/50063452/120926505-19261200-c718-11eb-9b08-57f8742a6fbc.png)
![Citeseer](https://user-images.githubusercontent.com/50063452/120926509-1c210280-c718-11eb-8e9f-b1119a0ce8ec.png)
