# Handling k samples  without replacement

### Algorithm(A-Res):

1. Initialize the reservoir with frist $k$ elements.     
($e_1 \text{ to } e_k$).

2. for e = $e_{k+1}...e_n$:
    1. give all element in the reservoir and $e$ a key : $key_i=r^{\frac{1}{wi}} ,r \in \text{uniform}[0,1]\text{ (=> key and r are positive correlation)}$
    2. find $k$ largest keys ,and update the reservoir to those corresponding elements.  
   
2. The final reservoir is the sampling result.


### Concept:
$X_i=r^{\frac{1}{w_i}},r\in uniform[0,1]$ 

$CDF(t) := Pr[X \leq t]=Pr[r^{\frac{1}{w_i}} \leq t]=Pr[r \leq t^{w_i}]=t^{w_i}$

$f_{x_i}(t):=PDF(t)=\frac{d(CDF(t))}{dt}=w_i* t^{w_i-1}$

$Pr[X_i \leq X_j]=	\int_{t_j=0}^1\int_{t_i=0}^{t_j}f_{x_i}(t_i)f_{x_j}(t_j)dt_idt_j$

$Pr[X_i \leq X_j]=\frac{w_j}{w_i+w_j}$.

Hence, the prob. of which key is larger is __positive correlated with the original weight__.

So the result of using A-Res algorithm is a Weighted Random Sampling (WRS).

### reference:
https://webdocs.cs.ualberta.ca/~mreza/courses/Streaming19/lecture10.pdf