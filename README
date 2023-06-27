This repository hosts the implementation of the masked minimizer optimization algorithm in the paper "Density and conservation optimization of the generalized masked-minimizer sketching scheme".

Basic usage:

A masked minimizer object can be created and trained using the following python script:

from config.std_config import *
from src.masked_minimizer import *

config = create config(...)
sketch = MaskedMinimizer(config)

where config is a python dictionary that contains the training configurations. config can be created by the function create_config that takes the following arguments: 

	- 'l': fragment length (input to the neural network)
	- 'w', 'k': window length and k-mer length of the masked minimizer scheme
	- 'mask': A PyTorch tensor of shape (w,) describing the mask parameter, default to the minimizer mask (e.g., torch.ones(w)). If 'mask' is not a PyTorch tensor the algorithm will optimize for it
	- 'seq': name of the sequence to be sketched. By default, sequences should be deposited at SEQ_DIR/[name].seq, where SEQ_DIR can be modified in utils/util.py
	- 'artifact_root': directory to folder where results will be saved to

Our experiment scripts can be found in the folder exp_scripts.
