The SorosimLinkage class allows the user to combine the previously defined [[SorosimLink]] objects into various linkages. The linkage topology may be open, closed, branched etc. The external forces and actuation is also defined in this class. The toolbox provides various inbuilt functions that allows the user to define various types of forces and moments, even custom external forces can be modelled. 

## Linkage definition
To define a SorosimLinkage S1 from previously defined Sorosims L1 and L2, we simply instatiate a Sorosimlinkage as follows
```
S1 = SorosimLinkage(L1,L2)
```
This leads the user to a GUI that allows the definition of relative position and orientation of the two links with respect to other links in the linkage. #todo ==add picture==

| Type | Name             | datatype | Description |
| ---- | ---------------- | -------- | ----------- |
|      | N                |          |             |
|      | ndof             |          |             |
|      | nsig             |          |             |
|      | VLinks           |          |             |
|      | LinkIndex        |          |             |
|      | CVTwists         |          |             |
|      | iLpre            |          |             |
|      | g_ini            |          |             |
|      | Z_order          |          |             |
|      |                  |          |             |
|      | nCLj             |          |             |
|      | iACL             |          |             |
|      | iCLB             |          |             |
|      | VTwistsCLj       |          |             |
|      | gACLj            |          |             |
|      | gBCLj            |          |             |
|      | CLprecompute     |          |             |
|      | T_BS             |          |             |
|      |                  |          |             |
|      | Gravity          |          |             |
|      | G                |          |             |
|      |                  |          |             |
|      | PointForce       |          |             |
|      | FollowerForce    |          |             |
|      | np               |          |             |
|      | Fp_loc           |          |             |
|      | Fp_vec           |          |             |
|      |                  |          |             |
|      | CEFP             |          |             |
|      | M_added          |          |             |
|      |                  |          |             |
|      | Actuated         |          |             |
|      | nact             |          |             |
|      |                  |          |             |
|      | Bqj1             |          |             |
|      | n_jact           |          |             |
|      | i_jact           |          |             |
|      | i_jactq          |          |             |
|      | Wrenchcontrolled |          |             |
|      |                  |          |             |
|      | n_sact           |          |             |
|      | dc               |          |             |
|      | dcp              |          |             |
|      | Sdiv             |          |             |
|      | Ediv             |          |             |
|      | Inside           |          |             |
|      | CableFunction    |          |             |
|      |                  |          |             |
|      | CAP              |          |             |
|      | CAS              |          |             |
|      |                  |          |             |
|      | K                |          |             |
|      | Damped           |          |             |
|      | D                |          |             |
|      |                  |          |             |
|      | CP1              |          |             |
|      | CP2              |          |             |
|      | CP3              |          |             |
|      |                  |          |             |
|      |                  |          |             |

## Class methods

>Bq = **ActuationMatrix**(Tr,q)
>**Input**: Tr ([[SorosimLinkage]]), q (generalised coordintes) 
>**Output**: Bq ()
>

>dqdt=**derivatives**(Tr,t,qqd,uqt)
>**Input**: Tr ([[SorosimLinkage]]), t(simulation time), qqd ( $\mathbb{R}^{2\times ndof}$ vector of generalised coordinates and its derivatives), ==uqt== 

>[t,qqd] = **dynamics**(Tr,qqd0,odetype,dt)

>E=**Equilibrium**(Tr,qu,uq,magnifier,lsqoptions)

>D = **findD**(Tr,varargin)

>K = **findK**(Tr,varargin)

>g = **FwdKinematics**(Tr,q,i_here,j_here)

>C = **GeneralizedCoriolisMatrix**(Tr,q,qd)

>F = **GeneralizedExternalForce**(Tr,q,t,qd)

>M = **GeneralizedMassMatrix**(Tr,q)

>J = **Jacobian**(Tr,q,i_here,j_here)

>Jd = **Jacobiandot**(Tr,q,qd,i_here,j_here)

>**plotq**(Tr,q)

>**plotq0**(Tr,Lh,Dh,CLh)

>**plotqqd**(Tr,t,qqd)

>xi = **ScrewStrain**(Tr,q,i_here,j_here)

>eta = **ScrewVelocity**(Tr,q,qd,i_here,j_here)

>[q,u]=**statics**(Tr,qu0,magnifier)
