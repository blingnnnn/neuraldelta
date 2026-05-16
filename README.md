# NeuralDelta

**Physics-Informed Neural Network for Probabilistic Flood Inundation Forecasting**  
Cagayan River Delta, Philippines

## Overview
NeuralDelta applies Physics-Informed Neural Networks (PINNs) to solve the 
2D Shallow Water Equations (SWE) for flood inundation prediction, integrating 
Sentinel-1 SAR flood observations as sparse data constraints and Monte Carlo 
Dropout for uncertainty quantification.

## Research Questions
1. Accuracy: Can NeuralDelta achieve CSI ≥ 0.70 vs. FEM benchmark?
2. Speed: Is NeuralDelta ≥ 50× faster than FEM at ≤ 100m resolution?
3. SAR fusion: Does λdata > 0 significantly reduce spatial RMSE?
4. Uncertainty: Are MC Dropout 95% credible intervals well-calibrated (≥ 80% coverage)?

## Study Area
Cagayan River Delta, Cagayan Valley, Philippines  
Target flood events: Typhoon Ulysses (Nov 2020), Typhoon Lawin (Oct 2016), 
Typhoon Mangkhut (Sep 2018)

## Environment Setup
```bash
conda create -n neuraldelta python=3.11 -y
conda activate neuraldelta
pip install torch --index-url https://download.pytorch.org/whl/cpu
pip install numpy scipy matplotlib rasterio pyproj shapely
pip install pandas xarray tqdm pyyaml mlflow jupyterlab ipykernel
```

## Repository Structure
See `docs/structure.md` for full description.

## License
MIT License — see LICENSE file.

## References
- Raissi et al. (2019), Journal of Computational Physics
- Mao et al. (2020), CMAME
- Bihlo & Popovych (2022), Journal of Computational Physics
- Chini et al. (2017), IEEE TGRS
- Gal & Ghahramani (2016), ICML