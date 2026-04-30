# DSPX Parameter Interpolation Algorithm 

## Overview 
In DSPX, the following interpolation algorithm is used to construct a smooth curve of the `hermit` interpolation type between two known points $(x_1, y_1)$ and $(x_2, y_2)$. This algorithm calculates derivatives using the Fritsch-Butland form via divided differences and performs piecewise cubic Hermite polynomial interpolation.

A C++ reference implementation can be found in `opendspx::interpolator` within [opendspx](https://github.com/diffscope/opendspx). 

## Input 
* **Endpoints**: $P_1(x_1, y_1)$, $P_2(x_2, y_2)$ 
* **Reference Points**: $P_{ref1}(x_{ref1}, y_{ref1})$, $P_{ref2}(x_{ref2}, y_{ref2})$ 

$P_{ref1}$ is the adjacent anchor node to the left of $P_1$, and $P_{ref2}$ is the adjacent parameter anchor node to the right of $P_2$.  If a curve exists between an endpoint and its reference point (regardless of that curve's interpolation type), the reference point should be provided as input to the algorithm; if no curve exists between them, the reference point is not input. 

## Output 
* A cubic polynomial function $H(x)$ defined on $[x_1, x_2]$. 

## Algorithm 

### Definitions

Define the **slope function**: 

$$\Delta(x_1, y_1, x_2, y_2) = \frac{y_1 - y_2}{x_1 - x_2}$$ 

Define the **derivative estimation function** $f_b(x_l, y_l, x, y, x_r, y_r)$:

Let:

$$h_l = x - x_l, \quad h_r = x_r - x$$ 

$$\delta_l = \Delta(x, y, x_l, y_l), \quad \delta_r = \Delta(x, y, x_r, y_r)$$ 

Defined as: 

$$f_b = \begin{cases} 0 & \text{if } \delta_l \cdot \delta_r \le 0 \\ \frac{3(h_l + h_r)}{\frac{2h_r + h_l}{\delta_l} + \frac{h_r + 2h_l}{\delta_r}} & \text{if } \delta_l \cdot \delta_r > 0 \end{cases}$$ 

### Calculations 

Calculate $d_1$: 

$$\begin{equation} d_1 = \begin{cases} fb(x_{ref1}, y_{ref1}, x_1, y_1, x_2, y_2) & \text{if } P_{ref1} \text{ exists} \\ \Delta(x_1, y_1, x_2, y_2) & \text{otherwise} \end{cases} \end{equation}$$

Calculate $d_2$: 

$$\begin{equation} d_2 = \begin{cases} fb(x_1, y_1, x_2, y_2, x_{ref2}, y_{ref2}) & \text{if } P_{ref2} \text{ exists} \\ \Delta(x_1, y_1, x_2, y_2) & \text{otherwise} \end{cases} \end{equation}$$

Next, based on the endpoint coordinates and derivatives $(x_1, y_1, d_1)$ and $(x_2, y_2, d_2)$, calculate the **intermediate parameters**: 

$$
\begin{align}
\delta &= \Delta(x_1, y_1, x_2, y_2)\\
c_0 &= y_1\\
c_1 &= d_1\\
c_2 = \delta_1^{(2)} &= \Delta(x_1, d_1, x_2, \delta)\\
\delta_2^{(2)} &= \Delta(x_1, \delta, x_2, d_2)\\
c_3 &= \Delta(x_1, \delta_1^{(2)}, x_2, \delta_2^{(2)})
\end{align}
$$ 

Define the **interpolation expression**: 

$$H(x) = a_3x^3 + a_2x^2 + a_1x + a_0$$ 

Where:

$$
\begin{align}
a_3 &= c_3 \\
a_2 &= c_2 - c_3(2x_1 + x_2) \\
a_1 &= c_1 - 2x_1c_2 + c_3(x_1^2 + 2x_1x_2) \\
a_0 &= c_0 - x_1c_1 + x_1^2c_2 - x_1^2x_2c_3
\end{align}
$$
