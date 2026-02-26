# Chapter 1

## Problem 1.1

Prove:

$$
[AB,CD] = -AC(D,B) + A(C,B)D - C(D, A)B +(C, A)DB
$$

## Solution:



By the definition of the commutator we can write the left hand side of our equality as: 

$$
[AB,CD] = ABCD - CDAB
$$

The terms on the right hand side of the equality may be expanded as follows:

$$
\begin{equation}
\begin{split}
{} -AC(D,B) &= {} - ACDB - ACBD \\\\
{} +A(C,B)D &= {} + ACBD + ABCD \\\\
{} -C(D,A)B &= {} - CDAB - CADB \\\\
{} +(C,A)DB &= {} + CADB + ACDB
\end{split}
\end{equation}
$$

Substituting:

$$
\begin{equation}
\begin{split}
{} - AC(D,B) + A(C,B)D - C(D,A)B + (C,A)DB &= {} - \cancel{ACDB} - \cancel{ACBD} \\\\
& \quad {} + \cancel{ACBD} + ABCD \\\\
& \quad {} - CDAB - \cancel{CADB} \\\\
& \quad {} + \cancel{CADB} + \cancel{ACDB} \\\\\\
&= ABCD - CDAB
\end{split}
\end{equation}
$$


$$
\begin{align*}
{}-AC(D,B) + A(C,B)D - C(D,A)B + (C,A)DB &= - \cancel{ACDB} - \cancel{ACBD} + \cancel{ACBD} + ABCD - CDAB - \cancel{CADB} + \cancel{CADB} + \cancel{ACDB} \\\\\\
&= {} ABCD - CDAB
\end{align*}
$$

Therefore: 

$$
[AB,CD] = -AC(D,B) + A(C,B)D - C(D, A)B +(C, A)DB
$$

## Problem 1.2

Suppose a 2×2 matrix $X$ (not necessarily Hermitian or unitary) is written as

$$
X = a_0 + \vec{σ} · \vec{a}
$$

where $a_0$ and $a_{1,2,3}$ are numbers.

(a) How are $a_0$ and $a_k(k = 1,2,3)$ related to $tr(X)$ and $tr(σ_k X)$ ?

(b) Obtain $a_0$ and $a_k$ in terms of the matrix elements $X_{ij}$.

## Solution:

(a) How are $a_0$ and $a_k(k = 1,2,3)$ related to $tr(X)$ and $tr(σ_k X)$ ?

$\vec{a}$ is a vector with elements $(a_1,a_2,a_3)$. $\vec{\sigma}$ is a 2 by 2 "Pauli vector" $(\vec{\sigma }=\sigma _{x}\vec{i}+\sigma _{y}\vec{j}+\sigma _{z}\vec{k})$ 

We calculate the dot product of $\vec{\sigma}$  and $\vec{a}$ as 

$$
\vec{\sigma} \cdot \vec{a} = [\sigma_1 \cdot a_1 + \sigma_2 \cdot a_2 + \sigma_3 \cdot a_3]
$$

We also can evaluate $tr(I_2) = 2$,  $tr(\sigma_j) = 0$, and $tr(\sigma_j \cdot \sigma_k) = 2\sigma_{jk}$ 

Now let

$$
X = a_0I_2 + \sum_{j=1}^3{\sigma_j  a_j}
$$

Taking the trace we get 

$$tr(X) = tr(a_0I_2) + \sum_{j=1}^{3}{a_j \cdot tr(\sigma_j)}$$

$$tr(X) = 2a_0$$

Thus,

$$\boxed{a_0 = \frac{1}{2} tr(X)}$$

To find

$$
tr(σ_k X) = a_0tr(\sigma_k)+ \sum_{j=1}^{3}{a_j \cdot tr(\sigma_k\sigma_j)}
$$

$$
tr(\sigma_kX) = 0 + \sum_{j=1}^{3}{a_j \cdot 2\sigma_{jk}} = 2a_k
$$

Therefore $\boxed{a_k = \frac{1}{2} tr(\sigma_kX), k=(1,2,3)}$ 

(b)

We start by writing 

$$
X = \begin{bmatrix}
			X_{11}  X_{12}\\
			X_{21}  X_{22}
		\end{bmatrix}
$$

We also know 

$$
\sigma_i = \begin{bmatrix} 0 &1 \\ 1& 0 \end{bmatrix} \sigma_j = \begin{bmatrix} 0 &-i \\ i &0 \end{bmatrix} \sigma_k = \begin{bmatrix} 1 & 0 \\ 0 &-1 \end{bmatrix}
$$

The expansion of X can be written as  

$$
X=a_0 ​I + a_1 ​σ_i​+ a_2 ​σ_j​ +a_3​ σ_k
$$

$$
a_0I = \begin{bmatrix} a_0 &0 \\ 0 & a_0 \end{bmatrix} \text{, }  a_1\sigma_i = \begin{bmatrix} 0 & a_1 \\ a_1 & 0\end{bmatrix}\text{, } a_2\sigma_j = \begin{bmatrix} 0 & -ia_2 \\ ia_2 & 0\end{bmatrix} \text{, } a_3\sigma_k=\begin{bmatrix} a_3 & 0 \\ 0 & -a_3 \end{bmatrix}
$$

Combined we write

$$
X = \begin{bmatrix} a_0+a_3 & a_1-ia_2 \\ a_1 + ia_2 & a_0 - a_3 \end{bmatrix}
$$

$$
{a_0 = X_{11} - a_3 \text{, } \space a_1 = X_{12} + ia_2 \text{, }\space a_2 = \frac{X_{21} - a_1}{i} \text{, } \space a_3 = a_0 - X_{22}}
$$


$$
\boxed{a_0 = \frac{X_{11} + X_{22}}{2}}
$$

$$
\boxed{a_1 = \frac{X_{12} + X_{21}}{2}}
$$

$$
\boxed{a_2= \frac{X_{21}-X_{12}}{2i}}
$$

$$
\boxed{a_3= \frac{X_{11}-X_{22}}{2}}
$$


## Problem 1.3

Show that the determinant of a 2×2 matrix $\sigma \cdot a$  is invariant under

$$
\vec{\sigma} \cdot \vec{a} \rightarrow \vec{\sigma} \cdot \vec{a^{`}} \equiv \exp(\frac{i\vec{\sigma}\cdot \hat{n} \phi}{2})\vec{\sigma} \cdot \vec{a}\exp(\frac{-i\vec{\sigma} \cdot \hat{n}\psi}{2})
$$

$a_k^{`}$ in terms of $a_k$ when $\hat{n}$ is in the positive z-direction, and interpret your result.

## Solution



## Problem 1.4

Using the rules of bra-ket algebra, prove or evaluate the following:

(a) $tr(XY) =  tr(YX)$, where X and Y are operators.

(b) $(XY)^{†} = Y^{†}X^{†}$ , where X and Y are operators.

(c) $\text{exp} \left[ if (A) \right] = ?$ in ket-bra form, where A is a Hermitian Operator whose eigenvalues are known.

(d) $\sum_{a^{\prime}} \psi_{a^{\prime}}^*\left(\mathbf{x}^{\prime}\right) \psi_{a^{\prime}}\left(\mathbf{x}^{\prime \prime}\right) \text {, where } \psi_{a^{\prime}}\left(\mathbf{x}^{\prime}\right)=\braket{\mathbf{x}^{\prime} | a^{\prime}} \text {. }$ 

## Solution

(a) Prove $tr(XY) =  tr(YX)$, where X and Y are operators. 

Assuming $X$ and $Y$ are both m by m matrices we write

$$
tr(X) = \sum_{i=1}^{m}{X_{ii}}
$$

and for a multiplication we know

$$
tr(XY) = \sum_{i=1}^{m}\sum_{j=1}^{m}X_{ij}Y_{ij}
$$

Since scalar multiplication is commutative we could re-arrange $X_{ij}$ and $Y_{ij}$ 

(b) $(XY)^{†} = Y^{†}X^{†}$ , where X and Y are operators.

Since $X$ and $Y$ are operators we can write

$$
XY\ket{a} = X(Y\ket{a}) \xleftrightarrow{DC} (\bra{a} Y^{\dagger})X^{\dagger} = \bra{a}Y^{\dagger}X^{\dagger}
$$

This shows that if we take the Hermitian of the product of two operators $X$ and $Y$ in that order, we will get $Y^{\dagger}X^{\dagger}$ 

(c)  exp(i f(A))) =? in ket-bra form, where A is a Hermitian Operator whose eigenvalues are known.

Firstly we know $A\ket{a'} = a'\ket{a'}$ and $\sum_{a'}\ket{a'}\bra{a'} =1$ 

Using this we get 

$$
A = \sum_{a'}{a'\ket{a'}\bra{a'}}
$$

So when we take $f(A)$ we get

$$
f(A)\ket{a'} = f(a')\ket{a'}
$$

and 

$$
f(A) = \sum_{a'}f'(a')\ket{a'}\bra{a'}
$$

Using the power series expansion of $e^x$ we write

$$
e^{if(A)} = \sum_{n=0}^{\infty}{\frac{(if(A))^n}{n!}} \rightarrow e^{if(A)} \ket{a'} = \sum_{n=0}^{\infty} \frac{i^n \cdot f(A)^n}{n!}\ket{a'} = \sum_{n=0}^{\infty} \frac{i^n \cdot f(a')^n}{n!}\ket{a'}
$$

So we know that

$$
e^{if(A)}\ket{a'} = e^{if(a')}\ket{a'}
$$

therefore the operator must be 

$$
\boxed{e^{if(a)}\ket{a'} = \sum_{a'}e^{if(a')}\ket{a'}\bra{a'}}
$$


## Problem 1.5

(a) Consider two kets $\ket{\alpha}$ and $\ket{\beta}$. Suppose $\braket{a' | \alpha},\braket{a'' | \alpha}, \ldots$ and $\braket{a' | \beta}$, $\braket{a'' | \beta}, \ldots$ are all known, where $\ket{a^{\prime}},\ket{a^{\prime \prime}}, \ldots$ form a complete set of base kets. Find the matrix representation of the operator $\ket{\alpha}\bra{\beta}$ in that basis.

(b) We now consider a spin $\frac{1}{2}$ system and let $\ket{\alpha}$ and $\ket{\beta}$ be $\ket{s_z=\hbar / 2}$ and $\ket{s_x=\hbar / 2}$, respectively. Write down explicitly the square matrix that corresponds to $\ket{\alpha}\bra{\beta}$ in the usual ( $s_z$ diagonal) basis.

## Solution

(a) 

$$
\ket{\alpha}\bra{\beta} \doteq\left(\begin{array}{ccc}
\braket{a^{(1)} | \alpha}\braket{a^{(1)} | \beta}^* & \braket{a^{(1)} | \alpha}\braket{a^{(2)} | \beta}^* & \ldots \\
\braket{a^{(2)} | \alpha}\braket{a^{(1)} | \beta}^* & \braket{a^{(2)} | \alpha}\braket{a^{(2)} | \beta}^* & \ldots \\
\vdots & \vdots & \ddots
\end{array}\right) .
$$

(b)

Let $\ket{\alpha} = S_{z}\ket{+} = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$ . We also know $\ket{\beta} = \ket{S_{x}+}$ so 

$$
S_{x} \ket{\beta} = \frac{\hbar}{2} \ket{\beta}
$$

$$
S_x = \frac{\hbar}{2}\begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
$$


Since we want $\ket{\beta}$ in the z basis we write

$$
\ket{\beta} = c_{+}\ket{+}+c_{-}\ket{-}
$$

so 

$$
\ket{\beta} = \begin{bmatrix} c_+ \\ c_- \end{bmatrix}
$$

Also

$$
S_x\ket{\beta} = \frac{\hbar}{2}\ket{\beta}
$$

Substituting the $S_x$ matrix in we get

$$
\frac{\hbar}{2}\begin{bmatrix} 0 &1 \\ 1 & 0 \end{bmatrix}\ket{\beta} = \frac{\hbar}{2} \ket{\beta}
$$

$$
\frac{\hbar}{2}\begin{bmatrix} 0 &1 \\ 1 & 0 \end{bmatrix} \begin{bmatrix} c_+ \\ c_-\end{bmatrix} = \frac{\hbar}{2} \begin{bmatrix} c_+ \\ c_-\end{bmatrix}
$$

Evaluating we get

$$
\begin{bmatrix} c_+ \\ c_-\end{bmatrix} = \begin{bmatrix} c_- \\ c_+\end{bmatrix}
$$

so $c_+ = c_- = a$

Taking the inner product of $\ket{\beta}$ with itself we must get 1 because the probability amplitude squared must be 1. 
so 

$$
\braket{\beta | \beta} = 1
$$

and that means that $|a|^2 + |a|^2 = 1$ or $a = \frac{1}{\sqrt{2}}$ . Therefore $\ket{\beta} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1\end{bmatrix}$. Now we can turn the ket $\ket{\beta}$ into a bra so that we can do outer product.

$$
\bra{\beta} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \end{bmatrix} 
$$

finally, 

$$
\ket{\alpha}\bra{\beta} = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \end{bmatrix} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \end{bmatrix}
$$



## Problem 1.6 

Suppose $\ket{i}$ and $\ket{j}$ are eigenkets of some Hermitian operator $A$. Under what condition can we conclude that  $\ket{i} + \ket{j}$ is also an eigenket of $A$? Justify your answer.

## Solution

Operator A  has eigenkets $\ket{i}$ and $\ket{j}$ so 

$$
A\ket{i} = a_{i}\ket{i}
$$

$$
A\ket{j} = a_{j}\ket{j} 
$$

So if we apply $A$ to the sum of the eigenkets 

$$
A(\ket{i}+\ket{j}) = A\ket{i}+A\ket{j} = a_{i}\ket{i} + a_{j}\ket{j}
$$

For $\ket{i}+\ket{j}$ to be an eigenket, it must fulfill the rule that $A(\ket{i}+\ket{j}) = \lambda (\ket{i}+\ket{j})$ 

Therefore 

$$
a_{i}\ket{i} + a_{j}\ket{j} = \lambda\ket{i}+\lambda \ket{j}
$$

must be true. 

Thus $a_i = a_j = \lambda$ . This means that the eigenvalues must be degenerate for  $\ket{i}+\ket{j}$ to be an eigenket of A.

## Problem 1.7 

Consider a ket space spanned by the eigenkets $\lbrace\ket{a'}\rbrace$ of a Hermitian operator $A$. There is no degeneracy.

(a) Prove that

$$
\prod_{a^{\prime}}\left(A-a^{\prime}\right)
$$

is the null operator.

(b) Explain the significance of

$$
\prod_{a^{\prime \prime} \neq a^{\prime}} \frac{\left(A-a^{\prime \prime}\right)}{\left(a^{\prime}-a^{\prime \prime}\right)} .
$$

(c) Illustrate (a) and (b) using $A$ set equal to $S_z$ of a spin $\frac{1}{2}$ system.

## Solution
