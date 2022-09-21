# ray tracing sphere with noise
# Xi Liu 2022
create ray traced sphere by solving ray sphere intersection equation</br>
using lambertian shading model with color $c$, diffuse reflectance $c_r$, and RGB intensity $c_i$, to account for ambient lighting such as skylight, add an ambient term $c_a$, $c = c_r(c_a + c_i \max(0, \textbf{n} \cdot \textbf{l}))$</br>
