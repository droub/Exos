# The Problème

Pour chaque fonction, donne les derivées du premier et second ordre:

```math
\begin{aligned}
f_1(x) &= \frac{3x+9}{2-x} \\
f_2(x) &= 3x \\
f_3(x) &= \sqrt{e^{2x}+2x} \\
f_4(x) &= e^{-x^2}(5x^3-7x) \\
\end{aligned}
```

Nota bene:
* $f''_3(x)$ trop dure ... laisse tomber

<details>
  <summary>Tips</summary>
  
```math
\begin{aligned}
&f'_1(1)=15 &f''_1(1)=30 \\
&f'_2(10)=3 &f''_2(-6)=0 \\
&f'_3(1/2)=\sqrt{e+1} &f''_3(1/2) = \frac{e^2-1}{(e+1)\sqrt(e+1)}\\
&f'_4(1)=12e &f''_4(1)=-6e \\
\end{aligned}
```
</details>

<details>
  <summary>Soluce</summary>
  
```math
\begin{aligned}
&f'_1(x) = \frac{15}{(2-x)^2}
&f''_1(x) = \frac{30}{(2-x)^3} \\
&f'_2(x) = x
&f''_2(x) = 0 \\
&f'_3(x) = \frac{e^{2x}+1}{\sqrt{e^{2x}+2x}}
&f''_3(x) = \frac{4e^{2x}x+e^{4x}-2e^{2x}-1}{(e^{2x}+2x)\sqrt{e^{2x}+2x}}\\
&f'_4(x) = e^{-x^2}(-10x^4+29x^2-7)
&f'_4(x) = e^{-x^2}(20x^5-98x^3+72x) \\
\end{aligned}
```
</detail>
