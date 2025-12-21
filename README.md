# Harnessing-Learnable-Wavelets-A-Lightweight-and-Effective-Model-for-Time-Series-Forecasting

## Abstract
Time series forecasting requires models that can efficiently capture complex temporal dependencies, especially in large-scale and high-dimensional settings.~While Transformer-based architectures excel at modeling long-range dependencies, their quadratic computational complexity poses limitations on scalability and adaptability. To address these challenges, we propose a lightweight model named Haar-TransF, a novel Transformer-inspired architecture that replaces the self-attention module with a learnable Multi-Scale Haar Transform (MSHT) block. The MSHT block, equipped with trainable low- and high-pass haar like filter coefficients, efficiently captures multi-scale approximation and detail components, effectively encoding periodic patterns while suppressing noise, thereby enhancing the modeling of correlations across multiple time series in forecasting tasks. Extensive experiments on several standard forecasting benchmarks demonstrate that Haar-TransF achieves superior predictive accuracy to conventional Transformer-based models, while substantially reducing memory usage for the time series forecasting task.~The obtained experimental results position Haar-TransF as a scalable and resource-efficient framework for advanced time series forecasting.

## 1. Proposed Framework
![Haar-TransF Architecture](assets/time_series_forecasting-Haar_Architecture.drawio.png)

*Figure 1 (a): Overview of the proposed Haar-TransF architecture.*

<p align="center">
  <img src="assets/time_series_forecasting-MSHT_block.drawio.png" 
       alt="Learnable Haar Wavelet"
       width="700">
</p>


## 2. Dataset
The performance of the proposed model is assessed on several benchmark time series forecasting datasets, namely Electricity \cite{wu2021autoformer}, Weather \cite{wu2021autoformer}, ETT \cite{zhou2021informer}, and PEMS \cite{chen2001freeway}. However, due to space constraints, we report results only for the ETTm1, ETTh1, and PEMS08 datasets. The (batch size, D-model) is set to (16, 512) for Electricity, (32, 768) for Weather,(32, 256) for ETTh1, (32, 256) for ETTm1, and (32, 640) for PEMS08 datasets, respectively, across all the experiments. The value of the number of heads is set to 16 for all the experiments.
| Dataset            | Variates | Timesteps | Granularity |
|--------------------|----------|-----------|-------------|
| Traffic            | 862      | 17,544    | 1 hour      |
| PEMS03             | 358      | 26,209    | 5 min       |
| PEMS04             | 307      | 16,992    | 5 min       |
| PEMS07             | 883      | 28,224    | 5 min       |
| PEMS08             | 170      | 17,856    | 5 min       |
| ETTm1 & ETTm2      | 7        | 17,420    | 15 min      |
| ETTh1 & ETTh2      | 7        | 69,680    | 1 hour      |
| Electricity        | 321      | 26,304    | 1 hour      |
| Exchange           | 8        | 7,588     | 1 day       |
| Weather            | 21       | 52,696    | 10 min      |
| Solar-Energy       | 137      | 52,560    | 10 min      |
