# LRGA-vessel
This is the LRGA method for ogbl-vessel.

## Dependencies: 
```{bash}
python==3.8
torch==1.10.1+cu102
torch-geometric==2.0.4
ogb==1.3.4
```

## Results on OGB-vessel:
Performance on **ogbl-vessel** (10 runs):

| Methods   | Test Acc  | Valid Acc  |
|  :----  | ---- | ---- |
| TAGConv (1-layers) |  OOM | OOM  |
| LRGA (1-layers) |  OOM | OOM  |
| SGC (3-layers) |  54.31 ± 23.79 | 54.33 ± 23.89  |
| SGC (3-layers w/o normalize) |  50.09 ± 0.11 | 50.10 ± 0.11  |


## Run Command:
```{bash}
python gnn.py --encoder='sgc' --decoder='mlp' --hidden_channels=16 --device=1  --lr=1e-6  --num_layers=3   --epochs=80
```
