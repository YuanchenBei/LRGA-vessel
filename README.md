# LRGA-vessel
This is the LRGA solution for [ogbl-vessel of the OGB Challenge](https://ogb.stanford.edu/docs/linkprop/#ogbl-vessel).


## Dependencies
```{bash}
python==3.8
torch==1.10.1+cu102
torch-geometric==2.0.4
ogb==1.3.4
```

## OGB Dateset
The dataset [ogbl-vessel](https://ogb.stanford.edu/docs/linkprop/#ogbl-vessel) should be download and placed in `./dataset/ogbl_vessel/`.


## Results on OGB-vessel
Performance on **ogbl-vessel** (10 runs):

Highest Train AUC: 50.64 ± 2.61

Highest Valid AUC: 54.18 ± 4.39

Final Train AUC: 47.84 ± 2.29

Final Test AUC: 54.15 ± 4.37


## Run Command
```{bash}
python gnn.py --encoder_name='lrga' --hidden_channels=16 --lr=1e-6 --num_layers=3 --epochs=100 --dropout=0.5
```


## Reference
[1] https://github.com/snap-stanford/ogb/tree/master/examples/linkproppred/vessel

[2] https://github.com/omri1348/LRGA
