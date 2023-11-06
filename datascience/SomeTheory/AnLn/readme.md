# Quiz2 
Proofing the bound of eigenvalue of $A_n$ and $L_n$.

### $A_n$:
$A_n=D^{\frac{-1}{2}}AD^{\frac{-1}{2}}\text{ (Normalized Adj. Matrix)}\in H$ with eigenvalues: $\alpha_1 \geq \alpha_2\geq ... \geq \alpha_n$

 
### $L_n$:
$L=D-A\text{ (Laplacian Matrix)}$,           
$L_n=I-A_n=D^{\frac{-1}{2}}LD^{\frac{-1}{2}}\text{ (Normailzed Laplacian Matrix)}$    
are both __Positive Semi-definite__

$\text{eigenvalues of } L_n :0\leq \lambda_{1} \leq...\leq \lambda_{n}$

$L$ has a eigenvector $\textbf{1}$ with corresponding eigenvalue = 0 (Sinece row sum = 0 for $L$)

## 1. Proof $\lambda_1=0$ :

Consider a vector : $x = D^{\frac{1}{2}}\textbf{1}$

$L_nx=D^{\frac{-1}{2}}LD^{\frac{-1}{2}}D^{\frac{1}{2}}\textbf{1}$

$=D^{\frac{-1}{2}}L\textbf{1}$    
and $L\textbf{1}=0$

$\Longrightarrow L_nx = 0$

$L_n$ has a eigenvalue 0 with corresponding eigenvector $D^{\frac{1}{2}}\textbf{1}$

and $L_n$ is PSD(i.e. 0 is the smallest eigenvalue)     
$\Longrightarrow \lambda_1 = 0$

## 2. Proof $\alpha_1 = 1$ :
$L_n$ is PSD : 

$x^TL_nx = x^T(I-A_n)x \geq 0$

$\Longrightarrow x^Tx - x^TA_nx\geq0$

$\Longrightarrow \frac{x^TA_nx}{x^Tx} \leq 1$

$\Longrightarrow \alpha_1 =  1 \text{ (Courant-Ficher Formula)}$

with corresponding eigenvector:

$x = D^{\frac{1}{2}}\textbf{1} : x^TL_nx=0 \Longrightarrow \frac{x^TA_nx}{x^Tx} = 1$

## 3. Proof $\alpha_n \geq -1$ :
Considering $I+A_n$ (is PSD,too):

$x^T(I+A_n)x \geq 0$

$\Longrightarrow x^TA_nx\geq -x^Tx$

$\Longrightarrow \frac{x^TA_nx}{x^Tx}\geq -1$

$\Longrightarrow \alpha_n \geq -1$

## 4. Proof $\lambda_n\leq2$

$x^T(I+A_n)x \geq 0$

$\Longrightarrow x^Tx \geq -x^TA_nx$

$\Longrightarrow 2x^Tx \geq x^Tx-x^TA_nx$

$\Longrightarrow 2 \geq \frac{x^T(I-A_n)x}{x^Tx}=\frac{x^TL_nx}{x^Tx}$

$\lambda_n \leq 2$

## Conclusion

$0 = \lambda_1 \leq \lambda_2 ... \leq \lambda_n \leq 2$

$1=\alpha_1 \geq \alpha_2 ... \geq \alpha_n \geq-1$

### Reference:
https://people.orie.cornell.edu/dpw/orie6334/Fall2016/lecture7.pdf