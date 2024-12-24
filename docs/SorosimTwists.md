# SoroSimTwists
The sorosimtwist class defines the degrees of freedom of a joint or a soft body. In the case of a rigid joint, it creates a base \(B\) matrix that consists of 1s and 0s that indicate which dof is allowed. A soft body has 6 modes of deformation, one torsion, two bending, one elongation and two shear. Bdof depending on the order of the polynomial used to fit the [strains](../strain parametrisation), we have two important parameters of the twists class called Bdof and Bodr that 

| Type | Name      | datatype | Description |
| ---- | --------- | -------- | ----------- |
|      | Type      |          |             |
|      | SubClass  |          |             |
|      | Bdof      |          |             |
|      | Bodr      |          |             |
|      | dof       |          |             |
|      |           |          |             |
|      | Bh        |          |             |
|      | B         |          |             |
|      | B_Z1      |          |             |
|      | B_Z2      |          |             |
|      | B_Z       |          |             |
|      |           |          |             |
|      | xi_starfn |          |             |
|      | xi_star   |          |             |
|      |           |          |             |
|      | Link      |          |             |
|      | div       |          |             |
|      | nip       |          |             |
|      | Xs        |          |             |
|      | Ws        |          |             |
|      | Ms        |          |             |
|      | Es        |          |             |
|      | Gs        |          |             |
|      |           |          |             |
|      | Xadd      |          |             |
|      | CI        |          |             |
|      | CIFn      |          |             |
## Class methods
>T = **jointtwist**(L,i)

>T = **jointtwist_pre**(L,i)

>[Ms,Es,Gs]= **MEG**(Link,j,Xs)

