# Basic functions

## adj = dinamico_adj(screw)
**Input**: A screw vector \\( \in\mathbb{R}^6 \\)<br>
**Ouput**: ==adjoint== 
Given a screw vector\\(\in \mathbb{R}^6\\), returns the adjoint, given by:
\\[ adj(S) = \begin{bmatrix}\tilde{w} & 0 \cr \tilde{v} &\tilde{w}\end{bmatrix}\\]


## Adj = **dinamico_Adjoint**(g)
Given an element in \\(SE(3)\\), returns the Adjoint.
\\[Ad(g) = \begin{bmatrix}\mathbf{R} & \mathbf{0} \cr \mathbf{\tilde{r}R} & \mathbf{R}\end{bmatrix}\\]

## coadj = **dinamico_coadj**(screw)
**Input**: A \\(\mathbb{R}^6\\) vector that represents a screw motion.<br>
**Output**: coadjoint representation
\\[ad^*(S) = \begin{bmatrix} \tilde{\omega} & \tilde{v} \cr \mathbf{0} & \tilde{\omega}\end{bmatrix}\\]

## coAdj = **dinamico_coAdjoint**(g)
**Input**: An \\(SE(3)\\) matrix<br>
**Output**: Coadjoint representations. 
\\[Ad^*(g) = \begin{bmatrix} \mathbf{R} & \mathbf{\tilde{r}R} \cr \mathbf{0} & \mathbf{R}\end{bmatrix}\\]

## skew = dinamico_tilde(vec)
**Input**: A vector in \\(\mathbb{R}^3\\)<br>
**Output**: Skew-symetric representation of the input<br>
For a vector \\(v\\), its cross product can be represented by a skew-symmetric matrix as:
\\[\tilde{v} = \begin{bmatrix} 0 && -v_3 && v_2 \cr v_3 && 0 && -v_1 \cr -v_2 && v_1 &&0\end{bmatrix}\\]
## se3 = dinamico_hat(screw)
**Input**: A vector in \\(\mathbb{R}^6\\)<br>
**Output**: \\(se(3)\\) representation of the vector<br>
The input vector must be of the form \\(\xi = [\mathbf{k}^T, \mathbf{p}^T]^T\\). The function converts it to the \\(se(3)\\) as:
$$ \hat{\xi} = \begin{bmatrix} \tilde{\mathbf{k}} && \mathbf{p} \cr \mathbf{0} && 0\end{bmatrix} $$ 


## [Xs,Ws,np]=**GaussQuadrature**(N_GQ)
**Input**: Number of quadrature points<br>
**Output**: Computed nodes, computed weights and the total number of points including the boundary points


## g = **ginv**(g)
**Input**: Transformation matrix in\\(SE(3)\\)<br>
**Output**: Inverse of the input


## xci=**piecewise_logmap**(g)
**Input**: Transformation matrix in\\(SE(3)\\)<br>

## g=**variable_expmap_g**(Gamma)

## [g,Tg]=**variable_expmap_gTg**(Gamma)

## [g,Tg,Tgd]=**variable_expmap_gTgTgd**(Gamma,Gammad)

## Texpg = **variable_Texpmap**(h,theta,Gamma)
