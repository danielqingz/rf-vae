# RF VAE
Pytorch implementation of RF_VAE proposed in Relevance Factor VAE: Learning and Identifying Disentangled Factors, Kim et al.([https://arxiv.org/abs/1902.01568])
<br>

### Dependencies
```
python 3.6.4
pytorch 0.4.0 (or check pytorch-0.3.1 branch for pytorch 0.3.1)
visdom
tqdm
```
<br>

### Datasets

```
NHATS
ACT_Slice
```
NOTE: I recommend to preprocess image files(e.g. resizing) BEFORE training and avoid preprocessing on-the-fly.
<br>

### Usage
initialize visdom
```
python -m visdom.server
```

e.g.
python main.py --name run_nhats --dataset nhats --gamma 6.4 --lr_VAE 1e-4 --lr_D 5e-5 --z_dim 10 ...
```
check training process on the visdom server
```
localhost:8097
```
<br>

##### visdom line plot
<p align="center">
<img src=result/Capture.PNG>
<img src=result/distribute.PNG>
</p>
##### latent traversal gif(```--save_output True```)
<p align="center">
<img src=result/random_img.gif>
<img src=result/fixed_heart.gif>
<img src=result/fixed_square.gif>
<img src=result/fixed_ellipse.gif>
</p>


##### reconstruction(left: true, right: reconstruction)
<p align="center">
<img src=result/300000.jpg>
</p>

### Reference
1. Relevance Factor VAE: Learning and Identifying Disentangled Factors.([https://arxiv.org/abs/1902.01568])
2. Explainable semi-supervised deep learning shows that dementia is associated with small, avocado-shaped clocks with irregularly placed hands ([https://www.nature.com/articles/s41598-023-34518-9])
