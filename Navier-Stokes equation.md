# Navier-Stokes equation

## 1.Conservation of Mass

### In a closed system, the total mass does not change with time, mass is conserved. <br>

$$ \frac{d}{dt} \iiint_V \rho dV = 0 $$

$$ = \iiint_V \frac{\partial p}{\partial t} dV + \iiint_V \nabla (\rho \vec{v}) $$ <br>
$$ = \iiint_V (\frac{\partial p}{\partial t} + \nabla (\rho \vec{v})) dV $$

### PDE for imcompressible fluids：<br>

$$ \nabla \vec{v} = 0 $$ <br>

### for imcompressible fluids

$$ \frac{d\rho}{dt}=0 \Rightarrow \rho \nabla \vec{v} = 0 \Rightarrow  \nabla \vec{v} = 0 $$

## 2.Conservation of Momentum

$$ \frac{d}{dt} \iiint_V \rho \vec{v} dV = \sum forces $$


 ### The forces consists of two parts: volume force and surface force .

### volume force:<br>

$$ \iiint_V \rho \,f dV $$ <br>

### the distribution of mass force :<br>

$$ f = f(x, y, z, t) $$


### surface force:<br>

$$ \oint\oint_S \vec{n} \sigma dS = \iiint_V \nabla \sigma dV $$<br>


### Final equation for the conservation of momentum :<br>

$$ \frac{d}{dt} \iiint_V \rho \vec{v} dV = \iiint_V \rho f dV + \iiint_V \nabla \sigma dV $$


