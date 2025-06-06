# Varion

Varion is a Python package designed to provide a high-quality and performant pseudo-random number generator (PRNG). It utilizes the xoshiro256** algorithm, which is known for its excellent statistical properties, large period, and high speed, making it particularly well-suited for demanding applications such as scientific simulations and exact sciences.

## Purpose

The primary goal of Varion is to offer a reliable source of randomness for Python applications where the quality and performance of random number generation are critical. Traditional PRNGs might not always meet the stringent requirements of certain scientific computations, and Varion aims to fill this gap by providing an accessible implementation of a modern and robust algorithm.

## How it Works

Varion uses the xoshiro256** (xor/shift/rotate/shift/rotate) algorithm. This algorithm is one of the latest in a family of PRNGs developed by David Blackman and Sebastiano Vigna. It generates 64-bit numbers and stands out due to its:

*   **Speed:** It's very fast, allowing for the generation of large volumes of random numbers quickly.
*   **Large Period:** The sequence of numbers it generates is extremely long before it repeats (2<sup>256</sup> - 1).
*   **Statistical Properties:** It passes numerous stringent statistical tests, ensuring the generated numbers have good randomness characteristics.

The package provides a simple function to get floating-point numbers in the range [0.0, 1.0).

## Installation

You can install Varion using pip:

```bash
pip install varion==0.1.0
```

## Usage Example

Here's a quick example of how to use Varion:

```python
from varion import varion_random

# Generate 10 random numbers using the default seed
random_numbers = varion_random(size=10)
print(random_numbers)

# Generate random numbers with a specific seed
seeded_numbers = varion_random(seed=12345, size=5)
print(seeded_numbers)
```

## Why Varion for Exact Sciences?

For disciplines like physics, cryptography, complex systems modeling, and advanced statistics, the quality of pseudo-random numbers is paramount. Biases or correlations in PRNGs can lead to incorrect simulation results, flawed analyses, or security vulnerabilities. Varion, by implementing xoshiro256**, offers:

*   **Reproducibility:** Essential for scientific experiments, achieved by setting a seed.
*   **High Dimensional Equidistribution:** Numbers are well-distributed, even when considering them in multiple dimensions.
*   **Reduced Bias:** Minimizes the risk of introducing systematic errors into calculations.

## Contributing

Contributions to Varion are welcome! If you have suggestions for improvements, bug fixes, or new features, please feel free to:

1.  Fork the repository on GitHub.
2.  Create a new branch for your changes.
3.  Make your changes, including tests if applicable.
4.  Submit a pull request for review.

Please ensure that your contributions align with the project's goals and maintain code quality.


---

## Resumen en Español

Varion es un paquete de Python diseñado para proporcionar un generador de números pseudoaleatorios (PRNG) de alta calidad y rendimiento. Utiliza el algoritmo xoshiro256**, conocido por sus excelentes propiedades estadísticas, su largo período y su alta velocidad, lo que lo hace especialmente adecuado para aplicaciones exigentes como simulaciones científicas y ciencias exactas.

### Propósito

El objetivo principal de Varion es ofrecer una fuente fiable de aleatoriedad para aplicaciones de Python donde la calidad y el rendimiento de la generación de números aleatorios son críticos.

### Instalación

Puedes instalar Varion usando pip:

```bash
pip install varion==0.1.0
```

### Contribuciones

¡Las contribuciones a Varion son bienvenidas! Si tienes sugerencias de mejora, correcciones de errores o nuevas características, por favor, siéntete libre de hacerlo a través de GitHub.
