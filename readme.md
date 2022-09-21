# ray tracing sphere with noise
# Xi Liu 2022
create ray traced sphere by solving ray sphere intersection equation</br>
represent sphere as a center $C$ and radius $r$, use 4 numbers $(C_x, C_y, C_z, r)$</br>
$(x - C_x) ^ 2 + (y - C_y) ^ 2 + (z - C_z) ^ 2 = r ^ 2$</br>
$\text{vector from center } \textbf{C} := (C_x, C_y, C_z) \text{ to point } \textbf{P} := (x, y, z) \text{ is } \textbf{P - C}$</br>
$\text{equation of sphere becomes }  \textbf{(P - C)} \cdot \textbf{(P - C)} = r ^ 2$</br>
$\text{if ray hits the sphere, then } \exists t, \textbf{P}(t) = \textbf{A} + t\textbf{b} \text{ that satisfies the sphere equation}$</br>
$\text{substitute } \textbf{P}(t) \text{ into the sphere equation }$</br>
$(\textbf{A} + t\textbf{b} - \textbf{C}) \cdot (\textbf{A} + t\textbf{b} - \textbf{C}) = r ^ 2$</br>
$((\textbf{A} - \textbf{C}) + t\textbf{b}) \cdot ((\textbf{A} - \textbf{C}) + t\textbf{b}) = r ^ 2$</br>
$\textbf{b} \cdot \textbf{b} t ^ 2 + 2\textbf{b} \cdot (\textbf{A} - \textbf{C}) t + (\textbf{A} - \textbf{C}) \cdot (\textbf{A} - \textbf{C}) - r ^ 2 = 0$</br>
$\text{solve for } t \text{ by using quadratic equation}$
using lambertian shading model with color $c$, diffuse reflectance $c_r$, and RGB intensity $c_i$, to account for ambient lighting such as skylight, add an ambient term $c_a$, $c = c_r(c_a + c_i \max(0, \textbf{n} \cdot \textbf{l}))$</br>
