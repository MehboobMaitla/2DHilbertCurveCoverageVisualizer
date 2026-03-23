# 2D Hilbert Curve Coverage Visualizer

**Hilbert-Augmented Reinforcement Learning for Multi-Robot Coverage**

## Overview 

This project visualizes how a **Hilbert space-filling curve** can optimize robot coverage of a 2D grid, compared to traditional naive **raster (boustrophedon) scan** patterns. It demonstrates the efficiency gains in path planning, reduced redundancy, and better spatial locality for multi-robot systems.

## Key Features

- **Hilbert Curve Generation** — Visualize space-filling curves at different orders (n = 1, 2, 3, 4)
- **Path Comparison** — Side-by-side analysis of Hilbert vs. Raster scanning patterns
- **Coverage Metrics** — Coverage efficiency, redundancy rates, and spatial locality scoring
- **Multi-Robot Partitioning** — Partition coverage space using Hilbert index splitting
- **Animated Visualization** — Watch robot paths unfold in real-time with interactive controls
- **Interactive Widgets** — Adjust parameters dynamically to explore different scenarios

## Concepts Covered

1. **Hilbert Space-Filling Curves**: Mathematical construction and properties
2. **Coverage Path Planning**: Comparison of different scanning strategies
3. **Efficiency Metrics**:
   - Coverage ratio (fraction of cells visited)
   - Redundancy rate (repeated cell visits)
   - Total distance traveled
   - Locality score (spatial clustering)
4. **Multi-Robot Coordination**: Efficient space partitioning via Hilbert indexing
5. **Visualization & Analysis**: Dynamic rendering and performance comparison

## Requirements

- Python 3.7+
- `hilbertcurve` — Hilbert space-filling curve implementation
- `matplotlib` — Static and animated visualizations
- `numpy` — Numerical computations
- `ipywidgets` — Interactive controls
- Jupyter Notebook or any compatible environment (Google Colab supported)

## Installation

### Quick Start (Auto-Install)

The notebook includes a setup cell that installs all dependencies:

```python
!pip install hilbertcurve matplotlib numpy ipywidgets --quiet
```

### Manual Installation

```bash
pip install hilbertcurve matplotlib numpy ipywidgets
```

## Usage

### Running the Notebook

1. **Google Colab** (recommended): Click the "Open In Colab" badge at the top of the notebook
2. **Local Jupyter**:
   ```bash
   jupyter notebook Hilbert_Curve_Coverage_Visualizer.ipynb
   ```

### Notebook Sections

| Cell | Description |
|------|-------------|
| 1-2 | Setup & dependency installation |
| 3 | Core functions: Hilbert path, raster path, metrics |
| 4 | Static comparison visualization |
| 5 | Coverage metrics analysis |
| 6 | Interactive path explorer widget |
| 7 | Multi-robot partitioning demo |
| 8 | Animated path traversal |
| 9 | Comprehensive comparison analysis |
| 10 | Performance benchmarking |

## Example Output

### Side-by-Side Comparison
The visualizer generates plots showing:
- **Left**: Hilbert curve path with traversal order colormapping
- **Right**: Raster scan pattern for comparison

### Metrics Display
Each path analysis shows:
- Coverage efficiency percentage
- Redundancy rates
- Total traversal distance
- Spatial locality score

### Multi-Robot Partition
Visualizes how the Hilbert index can efficiently partition a region among multiple robots.

## Project Structure

```
2DHilbertCurveCoverageVisualizer/
├── README.md                              # This file
└── Hilbert_Curve_Coverage_Visualizer.ipynb # Main notebook
```

## How Hilbert Curves Improve Coverage

### Advantages:
**Spatial Locality** — Consecutive cells are spatially close, minimizing backtracking  
**Low Redundancy** — Visits each cell exactly once in optimal cases  
**Scalability** — Easily extends to higher dimensions and larger grids  
**Multi-Robot Friendly** — Index-based partitioning enables balanced load distribution  

### vs. Raster Scanning:
- Hilbert curves maintain better spatial coherence
- Reduced total distance traveled
- Better energy efficiency for robot systems
- Improved coverage time for large-scale applications

## Applications

- **Autonomous Lawn Mowers** — Efficient grass mowing patterns
- **Drone Coverage** — UAV scanning of terrain or infrastructure
- **Industrial Robots** — Surface inspection and cleaning
- **Path Planning** — Multi-agent coordination
- **Satellite Imaging** — Grid-based area scanning

## Interactive Widgets

The notebook includes several interactive components:

1. **Order Selector** — Choose Hilbert curve order (1-4)
2. **Grid Visualizer** — Real-time path rendering
3. **Metrics Compare** — Toggle between different efficiency metrics
4. **Robot Count** — Adjust number of robots for partitioned coverage
5. **Animation Speed** — Control traversal animation playback

## Performance Notes

- **Order 1-3**: Instant computation and visualization
- **Order 4**: ~1-2 seconds rendering time (16×16 grid = 256 cells)
- **Higher Orders**: Not implemented (exponential grid growth)

## Contributing

This is an educational project. Suggestions and improvements are welcome!

### Possible Extensions:
- 3D Hilbert curve extension
- Cost-based path weighting
- Real-world robot simulation integration
- Comparison with other space-filling curves (Peano, Z-order, etc.)

## References

- [Hilbert Curve - Wikipedia](https://en.wikipedia.org/wiki/Hilbert_curve)
- [Space-Filling Curves and Data Indexing](https://en.wikipedia.org/wiki/Space-filling_curve)
- [Multi-Robot Coverage Path Planning](https://ieeexplore.ieee.org/document/7422630)
- [hilbertcurve Library](https://github.com/galtay/hilbertcurve)

## License

This project is provided for educational purposes.


