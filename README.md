# Solving the heat equation

The heat equation is a partial differential equation.

It is most commonly seen under its standard form in one dimension:

<p align="center">
    <img src="https://latex.codecogs.com/svg.latex?\frac{\partial%20u}{\partial%20t}%20=%20\alpha%20\frac{\partial^2%20u}{\partial%20x^2}" alt="1D Heat Equation">
    <br>
</p>

But it in higher dimensions it can be expressed as:

<p align="center">
    <img src="https://latex.codecogs.com/svg.latex?\frac{\partial%20u}{\partial%20t}%20=%20\alpha%20\nabla^2%20u" alt="Higher Dimensional Heat Equation">
    <br>
</p>

Where:
- `u(x, t)`: Temperature at position `x` and time `t`
- `α`: Thermal diffusivity of the material
- `∂u/∂t`: Rate of change of temperature with respect to time
- `∂²u/∂x²`: Second spatial derivative
- `∇²`: Laplace operator

It was first developed by French mathematician and physicist Joseph Fourier in 1822 for modelling how a quantity such as heat diffuses in a given region, but many great minds (such as Joule, Carnot, Kelvin... or even Benjamin Thompson, who measured heat produced during the process of boring a cannon) had worked on the concept of heat diffusion, from the Ancient Greeks to modern scientists. 

| Summary   |
|-----------|
| [Introduction](#Introduction) |
| [Newton-Raphson estimation method](#Newton-Raphson-estimation-method) |
| [Finding solution bounds](#Finding-solution-bounds) |
| [Deriving the heat equation in 1D](#Deriving-the-heat-equation-in-1-D)|
| [Generalizing the solution technique](#Generalizing-the-solution-technique) |
| [Computational methods](#Computational-methods) |
| [Optimization](#Optimization) |

## Introduction

As mentioned above, the heat equation is a partial differential equation which arises in problems of heat conduction.

At steady state, the heat equation simplifies down to Laplace's equation, a second order partial differential equation:

<p align="center">
    <img src="https://latex.codecogs.com/svg.latex?\nabla^2u%20=%200" alt="Laplace's Equation">
</p>

Where:
- `u`: Scalar potential function (e.g., temperature, electric potential, etc.)
- `∇²`: Laplace operator, defined as `∂²/∂x² + ∂²/∂y²` in 2D or `∂²/∂x² + ∂²/∂y² + ∂²/∂z²` in 3D

In effect, the heat equation can be thought of as an extension of Laplace's equation to include the effect of time-dependent heat flow. 

## Newton-Raphson estimation method

## Finding solution bounds

## Deriving the heat equation in 1D

Consider the temperature distribution u(x,t) in a thin metal rod of length L. 

<p align="center">
    <img src="https://github.com/user-attachments/assets/1f24faf7-305e-40d1-85f6-eb92d40e4cb2" alt="Metal Rod">
    <br>
</p>

The rate of change of heat energy in time is the sum of the heat flux through the boundary to its neighbours and the heat energy generated at any point in space/time. 
This equation is a general statement regarding the conservation of thermal energy. 

<!DOCTYPE html>
<html lang="en">
<body>
    <p>The formula for heat energy is given by:</p>
    <p>
        $$c(x) \rho(x) \frac{\partial u(x, t)}{\partial t} = -\frac{\partial q}{\partial x} + Q(x, t)$$
    </p>
    <p>
        <small>Where:</small>
        <ul>
            <li><code>c(x)</code>: Specific heat</li>
            <li><code>ρ(x)</code>: Density</li>
            <li><code>u(x, t)</code>: Internal energy</li>
            <li><code>q</code>: Heat flux</li>
            <li><code>Q(x, t)</code>: Heat source</li>
        </ul>
    </p>
</body>
</html>

From there, we have:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heat Flux Diagram</title>
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script type="text/javascript" id="MathJax-script" async
        src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
    </script>
</head>
<body>
    <h1>Heat Flux Diagram and Equations</h1>
    <div>
        <p>
            Heat flux, denoted as \( q(x, t) \), is the thermal energy transferred per unit time:
        </p>
        <p>
            \[
            q(x + \Delta x, t) = -k \frac{\partial u}{\partial x}
            \]
        </p>
        <p>
            The rate of change of heat flux is given by:
        </p>
        <p>
            \[
            -\frac{\partial q}{\partial x} = \lim_{\Delta x \to 0} \frac{q(x, t) - q(x + \Delta x, t)}{\Delta x}
            \]
        </p>
        <p>
            Here, \( k \) is the thermal conductivity, \( u \) is the temperature, and \( \Delta x \) is the small spatial increment.
        </p>
    </div>
</body>
</html>


Fourier worked on the heat equation (in fact he invented the Fourier transform as a tool to solve the heat equation) and derived Fourier's law of heat conduction, which we 

## Generalizing the solution technique

## Computational methods

## Optimization


