
> adj = **dinamico_adj**(screw)
**Input**: A screw vector $\in\mathbb{R}^6$ 
**Ouput**: ==adjoint== 
Given a screw vector $\in \mathbb{R}^6$ , returns the adjoint, given by:
$$adj(S) = \begin{bmatrix}[w] &0 \\ [v] &[w]\end{bmatrix}$$


>Adj = **dinamico_Adjoint**(g)
Given an element in $SE(3)$, returns the Adjoint.

> coadj = **dinamico_coadj**(screw)
**Input**: A $\mathbb{R}^6$ vector that represents a screw motion.
**Output**: coadjoint representation

> coAdj = **dinamico_coAdjoint**(g)
**Input**: An $SE(3)$ matrix
**Output**: Coadjoint representations. 
#todo put the equations for all of these representaions.

>[Xs,Ws,np]=**GaussQuadrature**(N_GQ)
**Input**: 

>g = **ginv**(g)

>xci=**piecewise_logmap**(g)

>g=**variable_expmap_g**(Gamma)

>[g,Tg]=**variable_expmap_gTg**(Gamma)

>[g,Tg,Tgd]=**variable_expmap_gTgTgd**(Gamma,Gammad)

>Texpg = **variable_Texpmap**(h,theta,Gamma)
