# Math Assessment 

This isn't for marks, it's just to make sure that there is enough background material in the course, and to help me plan the rest of the course. Your answer for each question should be a sentence or two. You do not have to write down any formulas, but you can if you choose to.

1. Consider 
   $$F(\omega)=\int^\infty_{-\infty} f(t)\exp\left(-i 2\pi \omega t\right) dt$$
    What is F called? What is the significance of $F$?

**Solution** : F is the Fourier Transform of $f$. If $f$ was broken up into oscillatory components, $F(\omega)$ would be proportional to the strength of the component oscillating with frequency $\omega$.

<br>
<br>

2. What is the general formula for a convolution? How does this relate to the previous question?

**Solution** : A convolution can be written: 
   $$(f*g)(y) = \int^{\infty}_{-\infty} f(x)g(y-x) dx$$
   The convolution theorem states that 
   $$F(f*g)=F(f)F(g)$$

<br>
<br>

3. How would you solve $\frac{dx}{dt} = -x + s(t)$ with initial condition $x(t_0)=x_0$? How would you interpret the meaning of the different terms in the equation.

**Solution** : The easiest way is to use an integrating factor. In this case we can multiply both sides of the equation by $e^t$, then rearrange and use the product rule: 

   $$\frac{d}{dt}\left(x e^t\right) = s(t)e^t$$
   Integrating both sides and doing some rearranging gives 
   
   $$x(t) = x_0 e^{t_0-t} + \int_{t_0}^t e^{t'-t} s(t') dt'$$

   The first term represents the initial condition, which decays with time. The second term represents the integrated affects of the forcing function $s$. Note that times farther away in the past contribute less to the present.

<br>
<br>

4. What does the equation $\partial_t C = \partial_{xx} C$ represent? If C is on a domain with no fluxes at the boundaries, describe what the solutions of C look like. 

**Solution** : This is the diffusion equation. The solutions will decay away from their initial condition towards the domain average of the inital condition.

**Aside**: If we assume the boundaries are at $-L$ and $L$, then we can write the boundary conditions as 

$$\partial_x C(-L)=\partial_x C(L)=0$$

If instead we were to use constant flux conditions, e.g. 

$$C(-L)=C(L)=0$$

 then the solutions will decay towards $0$ because the fluxes across $\pm L$ will equilibrate $C$.
<br>
<br>

5. What is the relationship that defines an eigenvalue and its associated eigenvector? 

**Solution** : For a given matrix $A$, if we denote the eigenvalues and eigenvectors as $\lambda_i$ and $\vec{p}_i$, Then these are defined by 
   $$A \vec{p}_i= \lambda_i \vec{p}_i$$ 
   
<br>
<br>

6. Suppose that a NxN matrix $A$ has N distinct eigenvalues and N linearly independent eigenvectors, how would you use them to rewrite $A$? What is useful about this new form?

**Solution** : If we put the eigenvalues and eigenvectors into matrices, $\Lambda = \mathrm{diag}(\lambda_1,...,\lambda_N)$, $P=\left[\vec{p}_1,...,\vec{p}_n\right]$, then 
   $$ A = P^{-1} \Lambda P$$ 
   This is a very useful form because 
   $$A^n = P^{-1} \Lambda^n P$$ 

