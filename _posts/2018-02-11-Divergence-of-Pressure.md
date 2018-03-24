---
layout: post
title: Divergence of the Pressure Tensor
use_math: true
---

Find an analytic expression for the divergence of the pressure tensor that separates the gyrotropic and non-gyrotropic terms.

$$
\overleftrightarrow{P} \equiv \begin{bmatrix}
P_{xx} & P_{xy} & P_{xz} \\
P_{yx} & P_{yy} & P_{yz} \\
P_{zx} & P_{zy} & P_{zz} \\
\end{bmatrix} \quad
\begin{array}{clr}
\textrm{a symmetric tensor of }\\
\textrm{pressure measurements}\\
\textrm{$P_{xy} = P_{yx}; P_{xz} = P_{zx}; P_{yz} = P_{zy}$}
\end{array}
$$

The definition of the divergence of the pressure tensor in matrix notation

$$
\div \overleftrightarrow{P} \equiv \begin{bmatrix}
\partial_x{P_{xx}} + \partial_x{P_{xy}} + \partial_x{P_{xz}} \\
\partial_y{P_{yx}} + \partial_y{P_{yy}} + \partial_y{P_{yz}} \\
\partial_z{P_{zx}} + \partial_z{P_{zy}} + \partial_z{P_{zz}} \\
\end{bmatrix}
 $$

Definition of the pressure tensor

$$
\begin{align}
\overleftrightarrow{P} &\equiv P_\parallel \hat b \hat b + P_\bot (\overleftrightarrow{I} - \hat b \hat b) + \overleftrightarrow{\Pi} \\
&^\text{(where $\hat b \hat b$ is a tensor)}
\end{align}
$$


Definition of the magnetic field direction tensor

$$
\begin{align}
\hat b \hat b = b_i b_j =
\begin{bmatrix}
b_x b_x & b_x b_y & b_x b_z \\
b_y b_x & b_y b_y & b_y b_z \\
b_z b_x & b_z b_y & b_z b_z
\end{bmatrix} \quad
\end{align}
$$

The perpendicular and parallel (to $$\hat b$$) components of the pressure tensor

$$
\begin{align}
P_\parallel &\equiv \hat b \vdot (\overleftrightarrow{P} \vdot \hat b)
\end{align}
$$

$$
\begin{align}
Tr(\overleftrightarrow{P}) &= 2 P_\bot + P_\parallel %\\ \notag
%&^\text{(where $\overleftrightarrow P$ has one axis aligned to $\hat b$)}
\end{align}
$$

$$
\begin{align}
P_\bot &= (\frac{(Tr(\overleftrightarrow{P}) - P_\parallel)}{2})
\end{align}
$$

In index notation, the pressure tensor becomes:

$$
\begin{align}
\overleftrightarrow{P} = P_{ij} \equiv
\underbrace{ P_\parallel b_i b_j + P_\bot (\var_{ij} - b_i b_j) }_{\text{gyrotropic}} +
\underbrace{\Pi_{ij}}_{\text{non-gyrotropic}
}
\end{align}
$$

We can then write the divergence of the pressure tensor:

$$
\begin{equation}
\div \overleftrightarrow P =
(\partial_i \overleftrightarrow P_{i j})_j =
\underbrace{ \partial_i (P_\parallel b_i b_j ) }_{P_\parallel [(\partial_i b_i) b_j ] + P_\parallel [ b_i (\partial_i b_j) ] +  b_i b_j (\partial_i P_\parallel)} +
\partial_i ( P_\bot [ \var_{i j} - b_i b_j]) +
\partial_i \Pi_{i j}
\end{equation}
$$

$$
\begin{equation}
\div \overleftrightarrow P =
(\partial_i \overleftrightarrow P_{i j})_j =
P_\parallel [(\partial_i b_i) b_j ] + P_\parallel [ b_i (\partial_i b_j) ] +  b_i b_j (\partial_i P_\parallel) +
\underbrace{ \underbrace{ \partial_i ( P_\bot [ \var_{i j} - b_i b_j]) }_{\partial_i P_\bot \var_{i j} - \partial_i [P_\bot b_i b_j]} }
  _{\partial_i P_\bot \var_{i j} - P_\bot [(\partial_i b_i) b_j ] - P_\bot [ b_i (\partial_i b_j) ] -  b_i b_j (\partial_i P_\bot)}
+ \partial_i \Pi_{ij}
\end{equation}
$$

$$
\begin{align}
\div \overleftrightarrow P =
(\partial_i \overleftrightarrow P_{i j})_j &=
P_\parallel [(\partial_i b_i) b_j ] + P_\parallel [ b_i (\partial_i b_j) ] +  b_i b_j (\partial_i P_\parallel) + \partial_i P_\bot \var_{i j} \\
&- P_\bot [(\partial_i b_i) b_j ] - P_\bot [ b_i (\partial_i b_j) ] -  b_i b_j (\partial_i P_\bot) \notag
+ \partial_i \Pi_{ij}
\end{align}
$$

Now we examine only the terms that contain the parallel pressure:

$$
\begin{align}
P_\parallel [(\partial_i b_i) b_j ] + P_\parallel [ b_i (\partial_i b_j) ] +  b_i b_j (\partial_i P_\parallel)
\end{align}
$$

The following is helpful for understanding the conversion from index notation to vector notation:

$$
\begin{align}
\text{Gradient} \quad \grad \vec a = \partial_i a_j =  \begin{bmatrix}
\partial_1{a_{1}} & \partial_1{a_{2}} & \partial_1{a_{3}} \\
\partial_2{a_{1}} & \partial_2{a_{2}} & \partial_2{a_{3}} \\
\partial_3{a_{1}} & \partial_3{a_{2}} & \partial_3{a_{3}} \\
\end{bmatrix} \quad \text{(rank = rank +1)}
\end{align}
$$

$$
\begin{align}
\text{Divergence} \quad \div \vec a = \partial_i a_i = scalar
 \quad \text{(rank = rank -1)}
\end{align}
$$

Converting the parallel pressure terms of $$\div \overleftrightarrow P$$ back to vector notation:

$$
\begin{align}
P_\parallel [(\div \hat b) \hat b ] + P_\parallel [ \hat b(\grad \hat b) ] +  \hat b \hat b (\grad P_\parallel)
\end{align}
$$

By looking at the rank of each section we can determine if we are missing any dot products.

$$
\begin{align}
P_\parallel \underbrace{[\underbrace{(\div \hat b)}_{\text{scalar}} \hat b ] }_{\text{vector}}
+ P_\parallel \underbrace{ [ \hat b \underbrace{ (\grad \hat b) }_{\text{tensor}} ] }_{\text{??}}
+  \underbrace{ \underbrace{\hat b \hat b}_{\text{tensor}} \underbrace{(\grad P_\parallel) }_{\text{vector}} }_{\text{Problem!}}
\end{align}
$$

The last two terms must be missing dot products that would reduce the rank...

$$
\begin{align}
P_\parallel \underbrace{[\underbrace{(\div \hat b)}_{\text{scalar}} \hat b ] }_{\text{vector}}
+ P_\parallel \underbrace{ [ \hat b \cdot \underbrace{ (\grad \hat b) }_{\text{tensor}} ] }_{\text{vector}}
+ \underbrace{\hat b \underbrace{(\hat b \vdot \grad P_\parallel) }_{\text{scalar}}}_{\text{vector}}
\end{align}
$$

where I have used the fact that a tensor inner product with a vector results in a vector (for the middle term).
Our final result for the parallel pressure components of $$\div \overleftrightarrow P$$ in vector notation is then

$$
\begin{align}
P_\parallel [(\div \hat b)\hat b
+ P_\parallel [ \hat b \cdot \grad \hat b]
+ \hat b (\hat b \vdot \grad P_\parallel)
\end{align}
$$

We can now use some useful definitions:

$$
\begin{align}
\vec \kappa \equiv \hat b \cdot \grad \hat b
\end{align}
$$

$$
\begin{align}
\div \vec B = 0
\end{align}
$$

where $$\vec \kappa$$ is the magnetic curvature. $$\vec \kappa$$ is positive pointing in toward the curvature focal point.

We can use Maxwell's equation for the divergence of the magnetic field to determine the divergence of the direction of the magnetic field.

$$
\begin{align}
\div \vec B = 0 \notag \\ \notag
\vec B = B \hat b \\ \notag
\div (B \hat b) = 0 \quad \text{or} \quad \partial_i (B b_i) = 0 \\ \notag
B (\div \hat b) + \hat b \cdot \grad B = 0 \quad \text{or} \quad B \partial_i b_i + b_i \partial_i B = 0
\end{align}
$$

Solving for $$\div \hat b$$:

$$
\begin{align}
\div \hat b = -\frac{\hat b \cdot \grad B}{B}  \quad \text{or} \quad \partial_i b_i = -\frac{b_i \partial_i B}{B} = 0
\end{align}
$$

Using these relations we then have:

$$
\begin{align}
\underbrace{P_\parallel [(\div \hat b)\hat b
+ P_\parallel [ \hat b \cdot \grad \hat b]
+ \hat b (\hat b \vdot \grad P_\parallel)}_{\downarrow} \\
P_\parallel [(-\frac{\hat b \cdot \grad B}{B})\hat b
+ P_\parallel \vec \kappa
+ \hat b (\hat b \vdot \grad P_\parallel)
\end{align}
$$

The divergence of the pressure tensor in index notation:

$$
\begin{align}
\div \overleftrightarrow P =
(\partial_i \overleftrightarrow P_{i j})_j &=
P_\parallel [-\frac{b_i \partial_i B}{B} ] b_j
+ P_\parallel \vec \kappa
+ b_i b_j (\partial_i P_\parallel)
+ \partial_i P_\bot \var_{i j} \\
&- P_\bot [(\partial_i b_i) b_j ]
- P_\bot [ b_i (\partial_i b_j) ]
-  b_i b_j (\partial_i P_\bot) \notag
+ \partial_i \Pi_{ij}
\end{align}
$$

The divergence of the pressure tensor in vector notation:

$$
\begin{align}
\div \overleftrightarrow P &=
P_\parallel [ \frac{-\hat b \cdot \grad B}{B}]\hat b
+ P_\parallel \vec \kappa
+(\hat b \cdot \grad P_\parallel) \hat b
+\grad P_\bot \overleftrightarrow I \\ \notag
&- P_\bot (\div \hat b) \hat b
- P_\bot (\hat b \cdot \grad \hat b)
-(\hat b \cdot \grad P_\bot) \hat b
+\div \overleftrightarrow \Pi
\end{align}
$$

Using the similarities in the structure, we can expand the $$- P_\bot (\div \hat b) \hat b$$ term exactly as we did before for $$P_\parallel$$.

$$
\begin{align}
-\underbrace{P_\bot [(\div \hat b)\hat b
- P_\bot [ \hat b \cdot \grad \hat b]
- (\hat b \vdot \grad P_\bot)\hat b}_{\downarrow} \\
-P_\bot [(-\frac{\hat b \cdot \grad B}{B})\hat b
- P_\bot \vec \kappa
- (\hat b \vdot \grad P_\bot)\hat b
\end{align}
$$

Our full expression for the divergence of the pressure tensor is then given by:

$$
\begin{align}
\div \overleftrightarrow P &=
P_\parallel [ \frac{-\hat b \cdot \grad B}{B}]\hat b
+ P_\parallel \vec \kappa
+(\hat b \cdot \grad P_\parallel) \hat b
+\grad P_\bot \\ \notag
&- P_\bot [(-\frac{\hat b \cdot \grad B}{B})\hat b
- P_\bot \vec \kappa
- (\hat b \vdot \grad P_\bot)\hat b
+\div \overleftrightarrow \Pi
\end{align}
$$

We look at each component to determine if they are parallel or perpendicular to the magnetic field direction $$\hat b$$.

$$
\begin{align}
\div \overleftrightarrow P &=
\underbrace{P_\parallel [ \frac{-\hat b \cdot \grad B}{B}]\hat b}_{\parallel}
+ \underbrace{P_\parallel \vec \kappa}_{\bot}
+\underbrace{(\hat b \cdot \grad P_\parallel) \hat b}_{\parallel}
+\underbrace{\grad P_\bot}_{\parallel \& \bot} \\ \notag
&- \underbrace{P_\bot [(-\frac{\hat b \cdot \grad B}{B})\hat b }_{\parallel}
- \underbrace{P_\bot \vec \kappa}_{\bot}
- \underbrace{(\hat b \vdot \grad P_\bot)\hat b}_{\parallel}
+\underbrace{\div \overleftrightarrow \Pi}_{\text{everything $\neq$ ($\parallel$ or $\bot$ ) }}
\end{align}
$$

We note that two terms can be combined:

$$
\begin{align}
\underbrace{\grad P_\bot}_{\grad_{total} P_\bot} - \underbrace{(\hat b \vdot \grad P_\bot)\hat b}_{\grad_\parallel P_\bot} = \grad_\bot P_\bot
\end{align}
$$

Rewritten:

$$
\begin{align}%[box=\widebox]
\div \overleftrightarrow P &=
\underbrace{
\underbrace{(P_\parallel - P_\bot) [ \frac{-\hat b \cdot \grad B}{B}]\hat b + (\hat b \cdot \grad P_\parallel) \hat b}_{\parallel} %\\ \notag
+ \underbrace{(P_\parallel - P_\bot) \vec \kappa +  \grad_\bot P_\bot}_{\bot}}_{\text{gyrotropic}}
+\underbrace{\div \overleftrightarrow \Pi}_{\text{non-gyrotropic}}
\end{align}
$$


