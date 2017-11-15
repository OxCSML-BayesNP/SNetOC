# SNetOC

Matlab package for Sparse and modular Networks with Overlapping Communities (SNetOC)

- Version: [v0.1.0](https://github.com/misxenia/SNetOC/releases/tag/v0.1.0)
- Last modified: 2017-11-08
- URL: <https://github.com/misxenia/SNetOC>

[**Download the package**](https://github.com/misxenia/SNetOC/archive/master.zip)

# Description

This Matlab package implements algorithms for simulation and posterior inference 
with the class of sparse graph models with overlapping community structure introduced by 
[Todeschini, Miscouridou and Caron (2017)](https://arxiv.org/abs/1602.02114). 
It allows to simulate graphs with a given level of sparsity and a deterministic number of communities.
It also performs inference of the network parameters (sociability parameters associated to nodes (multivariate vectors)) 
and to assess the sparsity of a given network.

The package has been tested on **Matlab R2016a**, **R2017a** and **R2017b** and requires the Statistics Toolbox.

# Reference

A. Todeschini, X. Miscouridou, F. Caron, _Exchangeable Random Measures for Sparse and Modular Graphs with Overlapping Communities_. **arXiv:1602.02114**. [Download paper](https://arxiv.org/abs/1602.02114 ).

# Installation

1. [Download the zip file](https://github.com/misxenia/SNetOC/archive/master.zip)
2. Unzip it in some folder
3. Run the test file `test.m`

In order to use the package, the folders `'GGP'`, `'CGGP'` and `'utils'` need 
to be added to the Matlab path, using the command `addpath` (see the test file).

# Contents

### Test script

- `test.m`: checks that the basic functions are running without error

### Demos and reproducible results of the article [Todeschini, Miscouridou and Caron (2017)](https://arxiv.org/abs/1602.02114)

- `demo_sparsity.m`: shows empirically the sparsity properties of a range of graph models. (see <https://github.com/misxenia/SNetOC/html/demo_sparsity.html>)

You can run multiple MCMC chains in parallel by calling the `parpool` command 
before running the following scripts. This requires the Parallel Computing Toolbox.

- `demo_simulations.m`: posterior inference on a simulated graph under the CCRM model. (see <https://github.com/misxenia/SNetOC/html/demo_simulations.html>)
- `demo_polblogs.m`: posterior inference on the polblogs graph under the CCRM model. (see <https://github.com/misxenia/SNetOC/html/demo_polblogs.html>)
- `demo_usairport.m`: posterior inference on the USairport graph under the CCRM model. (see <https://github.com/misxenia/SNetOC/html/demo_usairport.html>)
- `demo_overlappingcommunity.m`: posterior inference on a simulated graph from the CCRM model. (see <https://github.com/misxenia/SNetOC/html/demo_overlappingcommunity.html>)
- `MMSB_polblogs.m`: posterior inference on the polblogs graph the mixed membership stochastic blockmodel.
- `MMSB_usairport.m`: posterior inference on the USairport graph the mixed membership stochastic blockmodel.

### Main functions: simulation and posterior inference on graphs

- `overlapping_community_detection`: Wrapper function; takes a graph as input and returns the level of affiliation of each node to different communities
- `graphmodel`: creates a graph model object
- `graphrnd`: samples a graph
- `graphmcmc`: creates a MCMC object
- `graphmcmcsamples`: runs a MCMC algorithm for posterior inference on graphs
- `graphest`: returns point estimates of the graph parameters

# Changes

### [v0.1.0](https://github.com/misxenia/SNetOC/releases/tag/v0.1.0) (2017-10-16)

- First release of the package.

# Copyright

`SNetOC` is Copyright (c) 2016-2017 [A. Todeschini](http://adrien.tspace.fr) (<adrien.todeschini@gmail.com>), [X. Miscouridou](http://www.stats.ox.ac.uk/~miscouri/) (<xenia.miscouridou@spc.ox.ac.uk>) and [F. Caron](http://www.stats.ox.ac.uk/~caron/) (<caron@stats.ox.ac.uk>).
All Rights Reserved.
See the file `LICENSE.txt`.

`utils/munkres.m` is Copyright (c) 2009, Yi Cao.
All rights reserved. 
See the file `utils/munkres_license.txt`.

---------------------------------------------------------------------------
