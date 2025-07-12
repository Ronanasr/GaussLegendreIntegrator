# GaussLegendreIntegrator

## Description
This Python script calculates the moment of inertia (I_z) about the z-axis for a solid defined by the constraint `x + 2y + 3z ≤ 6` with a custom density function, using 3-point Gauss-Legendre quadrature for numerical integration. Additionally, it visualizes the solid as a 3D surface plot. The script leverages `numpy` for efficient computations and `matplotlib` for high-quality visualization. The resulting plot is saved as a PNG image.

## Features
- Computes the moment of inertia I_z using 3-point Gauss-Legendre quadrature.
- Visualizes the solid as a 3D surface plot with customizable settings (size, resolution, colormap).
- Saves the 3D plot as a high-quality PNG file.
- Employs vectorized operations and modular code for efficiency and readability.
- Supports a custom density function for flexible integration.

## Requirements
- Python 3.x
- Required libraries:
  - `numpy`
  - `matplotlib`

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/gauss-legendre-integrator.git
   ```
2. Navigate to the project directory:
   ```bash
   cd gauss-legendre-integrator
   ```
3. Install the required libraries:
   ```bash
   pip install numpy matplotlib
   ```

## Usage
1. Save the script as `inertia_calculator.py`.
2. Run the script:
   ```bash
   python inertia_calculator.py
   ```
3. The script will:
   - Calculate and print the moment of inertia (I_z) about the z-axis.
   - Generate a 3D surface plot of the solid defined by `x + 2y + 3z ≤ 6`.
   - Save the plot as `solid_plot.png` in the project directory.
   - Display the 3D plot.

## Example Output
Below is an example of the 3D surface plot for the solid:
![Solid Plot](solid_plot.png)

## Code Explanation
- **Function**: `density(x, y, z)`
  - Defines the density function `x^2 * y * z` for the solid.
- **Function**: `gauss_legendre_3d(func, x_limits, y_limits_func, z_limits_func)`
  - Computes a 3D integral using 3-point Gauss-Legendre quadrature.
  - Supports variable integration limits for y and z based on x and y, respectively.
- **Function**: `inertia_z()`
  - Calculates the moment of inertia I_z using the density function and Gauss-Legendre quadrature.
- **Function**: `plot_solid(figsize=(10, 8), dpi=300)`
  - Generates a 3D surface plot of the solid defined by `x + 2y + 3z ≤ 6`.
  - Saves the plot as a high-quality PNG file.
- **Key Parameters**:
  - `x_limits = [0, 6]`: x-axis bounds for integration.
  - `y_limits_func = lambda x: [0, (6 - x) / 2]`: y-axis bounds dependent on x.
  - `z_limits_func = lambda x, y: [0, (6 - x - 2 * y) / 3]`: z-axis bounds dependent on x and y.

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For questions or feedback, feel free to open an issue on GitHub or contact [ronasr82@gmail.com](mailto:ronasr82@gmail.com).
