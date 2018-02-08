# SCALP:

This repository provides a reference implementation of *SCALP*

The *SCALP* is a novel link prediction framework, by jointly modeling both user's social network relationship and spatiotemporal check-in information

Before to execute *SCALP*, it is necessary to install the following packages:
<br/>
``pip install futures``
<br/>
``pip install fastdtw``
<br/>
``pip install gensim``

## Requirements

-  numpy==1.13.1
-  networkx==2.0
-  scipy==0.19.1
-  tensorflow==1.3.0
-  gensim==3.0.1
-  scikit-learn==0.19.0

### Basic Usage

- --run /data_process/ by the following order:data_proper_time.py,data_filter.py and data_split.py
- --run /NE/ or /struc2vec to obtain the network representation. The detailed instructions see:
- --run /poissionmf/ by the following order:data_checkins.py and create_matrix to obtain the spatiotemporal check-in information representation
- --run /evaluate/ to estimate the performance of SCALP. The four_methods.py and model_mlp.py will generate four contrastive experiments. The lsh_joint.py and model_scalp.py is used to evaluate the *SCALP*

#### Options

- --You can choose the location range of check_ins or the check time by modify /data_process/data_proper_time.py
- --You can choose the number of user nodes(just sub-graph) by modify /data_process/data_filter.py
- --You can adjust the proportion of the training set and the test set by modify /data_process/data_split.py
- --You can choose /NE/ which includes:node2vec,line,deepWalk,grarep or /struc2vec/ which includes:struc2vec to generate the network representation

### Miscellaneous

*Note:* This is only a reference implementation of *SCALP*.
