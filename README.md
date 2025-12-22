# Harnessing-Learnable-Wavelets-A-Lightweight-and-Effective-Model-for-Time-Series-Forecasting
Code will be resealing soon..!!

##  Ablation
We compare the proposed model with several state-of-the-art (SOTA) approaches such as iTransformer [[Paper]](https://arxiv.org/abs/2306.06633), PatchTST [[Paper]](https://arxiv.org/abs/2211.14730), Crossformer [[Paper]](https://arxiv.org/abs/2303.01379), Autoformer [[Paper]](https://arxiv.org/abs/2106.13008), RLinear [[Paper]](https://arxiv.org/abs/2305.16397), TiDE [[Paper]](https://arxiv.org/abs/2304.08424), DLinear [[Paper]](https://arxiv.org/abs/2205.13504), FedFormer [[Paper]](https://arxiv.org/abs/2201.12740) and TimesNet [[Paper]](https://arxiv.org/abs/2210.02186). We evaluate model performances using Mean Squared Error (MSE) and Mean Absolute Error (MAE) between the ground truth and predictions.~Table.1 reports the comparative performance of Haar-TransF against state-of-the-art methods on five benchmark TSF datasets. The evaluation is conducted across multiple forecasting lengths, and the overall effectiveness is measured by averaging the MSE and MAE across all lengths. The table also reports the value of the parameter number of levels $(L)$ corresponding to the best results. Specifically, for the PEMS-8 dataset, the model attains its highest performance at level 4, whereas for most of the other datasets, the optimal performance is observed at level 1. As evident from the results, Haar-TransF consistently outperforms existing approaches, achieving 22 best MSEs and 20 best MAEs in total. On the Weather dataset, Haar-TransF delivers notable improvements of 0.09 in MSE and 0.04 in MAE over the i-Transformer. For the PEMS08 dataset, its performance remains competitive with i-Transformer. Crucially, unlike i-Transformer, which struggles to capture the inherent periodic structures of these datasets, Haar-TransF effectively leverages such patterns to attain superior forecasting accuracy. Furthermore, it demonstrates substantial gains over linear baseline such as RLinear, highlighting its ability to learn richer temporal representations.
<p align="center">
  <img src="assets/mian_table.png" 
       alt="main_results with baselines"
       width="800">
</p>

### Ablations
<p align="center">
  <img src="assets/HaarTransF_Ablation.png" 
       alt="main_results with baselines"
       width="400">
</p>
