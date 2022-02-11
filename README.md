
# Count-GNN
We provide the implementaion of Count-GNN model on Small,Large,MUTAG, OGB dataset.

The repository is organised as follows:
- data/: data/ only contains MUTAG data currently, we will upload other datasets later.
- count-gnn/: contains our model.
- converter/: contains code to convert graphs to igraph format
- generator/: contains code to generate queries and graphs



## Package Dependencies

* tqdm
* numpy
* pandas
* scipy
* tensorboardX
* torch >= 1.3.0
* dgl == 0.4.3post2

## Running experiments

To run _train.py:
- python _train.py --model EDGEMEAN --predict_net FilmSumPredictNet --emb_dim 4 --ppn_hidden_dim 12 --weight_decay_film 0.0001 --pattern_dir ../data/MUTAG/patterns --graph_dir ../data/MUTAG/raw --metadata_dir ../data/MUTAG/metadata --save_data_dir ../data/MUTAG --save_model_dir ../dumps/MUTAG/EDGEMEAN-FilmSumPredictNet1.1 --share_emb False &

To run evaluate.py:
- python evaluate.py ../dumps/MUTAG1000/EDGEMEAN-FilmSumPredictNet1.1

