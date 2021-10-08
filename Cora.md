## Changes made to apply to Cora

### Dataset
- new dataset wrapper for pyg dataset
- change node embedding layer dimensions
- TrucateData as pre_transform (optional) to sample smaller graph
- get dataset with cross_entropy loss and accuracy evaluator
- use train/val/test_mask when computing loss and accuracy

### No edge features
- new collator, ignoring edge features
- ignore edge features in Batch if None
- new preprocess method skipping edge features
- edge_type 'None' instead of 'Multihop' - edge features are not computed
- Do not edge features to attention mask
- no "gen_edge_input" - Problem?

## Node classification
- output layer that maps to 1x#nodesx#classes instead of 1x#classes
- adapt in forward, train_step, validation and test (step and epoch_end)