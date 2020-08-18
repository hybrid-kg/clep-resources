Datasets
---------
Datasets currently used in this repo

| Number | Dataset | Samples | Controls  |
| -- | -------------:|:-------------:| -----:|
| #1 | ADNI | 484 | 260 |


Repository Structure
---------------------
The repo contains a main folder ([Experiments](Experiments/)) containing 3 experiments that were carried out using
 [CLEP](https://github.com/hybrid-kg/clep) framework for each dataset.

The data and results for each experiment is available in their respective folders, within each dataset's folder,
1) [Benchmark](Experiments/ADNI/benchmarking) - Benchmarking experiment to check the performance of CLEP in contrast
 with the raw data (including robustness analysis),
2) [Kge_Model](Experiments/ADNI/kge_model) - Experiment to check the effect of KGE model on the classification, and
3) [Threshold](Experiments/ADNI/threshold) - Experiment to check the effect of threshold applied during the incorporation of
 patients in the KG.

Each experiment folder contains a data and results folder.

The tree structure looks like as given below,
```
Experiments/
└── ADNI
    ├── kge_model
    │   ├── data
    │   │   └── pathme.edgelist
    │   └── results
    │       ├── ComplEx
    │       │   ├── config.json
    │       │   ├── cross_validation_results.json
    │       │   ├── embedding.tsv
    │       │   ├── pykeen_results_final
    │       │   │   ├── metadata.json
    │       │   │   └── results.json
    │       │   ├── pykeen_results_optim
    │       │   │   ├── best_pipeline
    │       │   │   │   └── pipeline_config.json
    │       │   │   ├── study.json
    │       │   │   └── trials.tsv
    │       │   ├── test.edgelist
    │       │   ├── train.edgelist
    │       │   └── validation.edgelist
    │       ├── HolE
    │       │   ├── config.json
    │       │   ├── cross_validation_results.json
    │       │   ├── embedding.tsv
    │       │   ├── pykeen_results_final
    │       │   │   ├── metadata.json
    │       │   │   └── results.json
    │       │   ├── pykeen_results_optim
    │       │   │   ├── best_pipeline
    │       │   │   │   └── pipeline_config.json
    │       │   │   ├── study.json
    │       │   │   └── trials.tsv
    │       │   ├── test.edgelist
    │       │   ├── train.edgelist
    │       │   └── validation.edgelist
    │       ├── RotatE
    │       │   ├── config.json
    │       │   ├── cross_validation_results.json
    │       │   ├── embedding.tsv
    │       │   ├── pykeen_results_final
    │       │   │   ├── metadata.json
    │       │   │   └── results.json
    │       │   ├── pykeen_results_optim
    │       │   │   ├── best_pipeline
    │       │   │   │   └── pipeline_config.json
    │       │   │   ├── study.json
    │       │   │   └── trials.tsv
    │       │   ├── test.edgelist
    │       │   ├── train.edgelist
    │       │   └── validation.edgelist
    │       ├── TransE
    │       │   ├── config.json
    │       │   ├── cross_validation_results.json
    │       │   ├── embedding.tsv
    │       │   ├── pykeen_results_final
    │       │   │   ├── metadata.json
    │       │   │   └── results.json
    │       │   ├── pykeen_results_optim
    │       │   │   ├── best_pipeline
    │       │   │   │   └── pipeline_config.json
    │       │   │   ├── study.json
    │       │   │   └── trials.tsv
    │       │   ├── test.edgelist
    │       │   ├── train.edgelist
    │       │   ├── validation.edgelist
    │       │   └── weighted.edgelist
    │       ├── network_summary.tsv
    │       ├── radical_summary.tsv
    │       ├── sample_scoring.tsv
    │       └── weighted.edgelist
    ├── benchmarking
    │   ├── data
    │   │   └── embedding.tsv
    │   └── results
    │       ├── emb
    │       │   ├── elastic_net
    │       │   │   └── grid_search
    │       │   │       └── cross_validation_results.json
    │       │   ├── gradient_boost
    │       │   │   └── grid_search
    │       │   │       └── cross_validation_results.json
    │       │   ├── logistic_regression
    │       │   │   └── grid_search
    │       │   │       └── cross_validation_results.json
    │       │   ├── random_forest
    │       │   │   └── grid_search
    │       │   │       └── cross_validation_results.json
    │       │   └── svm
    │       │       └── grid_search
    │       │           └── cross_validation_results.json
    │       ├── perm
    │       │   ├── elastic_net
    │       │   │   └── grid_search
    │       │   │       └── cross_validation_results.json
    │       │   ├── gradient_boost
    │       │   │   └── grid_search
    │       │   │       └── cross_validation_results.json
    │       │   ├── logistic_regression
    │       │   │   └── grid_search
    │       │   │       └── cross_validation_results.json
    │       │   ├── random_forest
    │       │   │   └── grid_search
    │       │   │       └── cross_validation_results.json
    │       │   └── svm
    │       │       └── grid_search
    │       │           └── cross_validation_results.json
    │       └── raw
    │           ├── elastic_net
    │           │   └── grid_search
    │           │       └── cross_validation_results.json
    │           ├── gradient_boost
    │           │   └── grid_search
    │           │       └── cross_validation_results.json
    │           ├── logistic_regression
    │           │   └── grid_search
    │           │       └── cross_validation_results.json
    │           ├── random_forest
    │           │   └── grid_search
    │           │       └── cross_validation_results.json
    │           └── svm
    │               └── grid_search
    │                   └── cross_validation_results.json
    └── threshold
        ├── data
        │   └── pathme.edgelist
        └── results
            ├── 1
            │   ├── RotatE
            │   │   ├── cross_validation_results.json
            │   │   ├── embedding.tsv
            │   │   ├── pykeen_results_final
            │   │   │   ├── metadata.json
            │   │   │   └── results.json
            │   │   ├── pykeen_results_optim
            │   │   │   ├── best_pipeline
            │   │   │   │   └── pipeline_config.json
            │   │   │   ├── study.json
            │   │   │   └── trials.tsv
            │   │   ├── test.edgelist
            │   │   ├── train.edgelist
            │   │   └── validation.edgelist
            │   ├── cross_validation_results.json
            │   ├── embedding.tsv
            │   ├── network_summary.tsv
            │   ├── pykeen_results_final
            │   │   ├── metadata.json
            │   │   └── results.json
            │   ├── pykeen_results_optim
            │   │   ├── best_pipeline
            │   │   │   └── pipeline_config.json
            │   │   ├── study.json
            │   │   └── trials.tsv
            │   ├── radical_summary.tsv
            │   ├── sample_scoring.tsv
            │   ├── test.edgelist
            │   ├── train.edgelist
            │   ├── validation.edgelist
            │   └── weighted.edgelist
            ├── 1.5
            │   ├── RotatE
            │   │   ├── cross_validation_results.json
            │   │   ├── embedding.tsv
            │   │   ├── pykeen_results_final
            │   │   │   ├── metadata.json
            │   │   │   └── results.json
            │   │   ├── pykeen_results_optim
            │   │   │   ├── best_pipeline
            │   │   │   │   └── pipeline_config.json
            │   │   │   ├── study.json
            │   │   │   └── trials.tsv
            │   │   ├── test.edgelist
            │   │   ├── train.edgelist
            │   │   └── validation.edgelist
            │   ├── cross_validation_results.json
            │   ├── embedding.tsv
            │   ├── network_summary.tsv
            │   ├── pykeen_results_final
            │   │   ├── metadata.json
            │   │   └── results.json
            │   ├── pykeen_results_optim
            │   │   ├── best_pipeline
            │   │   │   └── pipeline_config.json
            │   │   ├── study.json
            │   │   └── trials.tsv
            │   ├── radical_summary.tsv
            │   ├── sample_scoring.tsv
            │   ├── test.edgelist
            │   ├── train.edgelist
            │   ├── validation.edgelist
            │   └── weighted.edgelist
            ├── 10
            │   ├── RotatE
            │   │   ├── cross_validation_results.json
            │   │   ├── embedding.tsv
            │   │   ├── pykeen_results_final
            │   │   │   ├── metadata.json
            │   │   │   └── results.json
            │   │   ├── pykeen_results_optim
            │   │   │   ├── best_pipeline
            │   │   │   │   └── pipeline_config.json
            │   │   │   ├── study.json
            │   │   │   └── trials.tsv
            │   │   ├── test.edgelist
            │   │   ├── train.edgelist
            │   │   └── validation.edgelist
            │   ├── embedding.tsv
            │   ├── network_summary.tsv
            │   ├── pykeen_results_final
            │   │   ├── metadata.json
            │   │   └── results.json
            │   ├── pykeen_results_optim
            │   │   ├── best_pipeline
            │   │   │   └── pipeline_config.json
            │   │   ├── study.json
            │   │   └── trials.tsv
            │   ├── radical_summary.tsv
            │   ├── sample_scoring.tsv
            │   ├── test.edgelist
            │   ├── train.edgelist
            │   ├── validation.edgelist
            │   └── weighted.edgelist
            ├── 2.5
            │   ├── RotatE
            │   │   ├── cross_validation_results.json
            │   │   ├── embedding.tsv
            │   │   ├── pykeen_results_final
            │   │   │   ├── metadata.json
            │   │   │   └── results.json
            │   │   ├── pykeen_results_optim
            │   │   │   ├── best_pipeline
            │   │   │   │   └── pipeline_config.json
            │   │   │   ├── study.json
            │   │   │   └── trials.tsv
            │   │   ├── test.edgelist
            │   │   ├── train.edgelist
            │   │   └── validation.edgelist
            │   ├── TransE
            │   │   ├── cross_validation_results.json
            │   │   ├── embedding.tsv
            │   │   ├── pykeen_results_final
            │   │   │   ├── metadata.json
            │   │   │   └── results.json
            │   │   ├── pykeen_results_optim
            │   │   │   ├── best_pipeline
            │   │   │   │   └── pipeline_config.json
            │   │   │   ├── study.json
            │   │   │   └── trials.tsv
            │   │   ├── test.edgelist
            │   │   ├── train.edgelist
            │   │   └── validation.edgelist
            │   ├── cross_validation_results.json
            │   ├── embedding.tsv
            │   ├── multi_res
            │   │   ├── elastic_net
            │   │   │   └── grid_search
            │   │   │       └── cross_validation_results.json
            │   │   ├── gradient_boost
            │   │   │   └── grid_search
            │   │   │       └── cross_validation_results.json
            │   │   ├── logistic_regression
            │   │   │   └── grid_search
            │   │   │       └── cross_validation_results.json
            │   │   ├── random_forest
            │   │   │   └── grid_search
            │   │   │       └── cross_validation_results.json
            │   │   └── svm
            │   │       └── grid_search
            │   │           └── cross_validation_results.json
            │   ├── network_summary.tsv
            │   ├── pykeen_results_final
            │   │   ├── metadata.json
            │   │   └── results.json
            │   ├── pykeen_results_optim
            │   │   ├── best_pipeline
            │   │   │   └── pipeline_config.json
            │   │   ├── study.json
            │   │   └── trials.tsv
            │   ├── radical_summary.tsv
            │   ├── sample_scoring.tsv
            │   ├── test
            │   │   ├── diff.txt
            │   │   ├── patient_connection_summary.tsv
            │   │   └── weighted.edgelist
            │   ├── test.edgelist
            │   ├── train.edgelist
            │   ├── validation.edgelist
            │   └── weighted.edgelist
            ├── 20
            │   ├── RotatE
            │   │   ├── cross_validation_results.json
            │   │   ├── embedding.tsv
            │   │   ├── pykeen_results_final
            │   │   │   ├── metadata.json
            │   │   │   └── results.json
            │   │   ├── pykeen_results_optim
            │   │   │   ├── best_pipeline
            │   │   │   │   └── pipeline_config.json
            │   │   │   ├── study.json
            │   │   │   └── trials.tsv
            │   │   ├── test.edgelist
            │   │   ├── train.edgelist
            │   │   └── validation.edgelist
            │   ├── embedding.tsv
            │   ├── network_summary.tsv
            │   ├── pykeen_results_final
            │   │   ├── metadata.json
            │   │   └── results.json
            │   ├── pykeen_results_optim
            │   │   ├── best_pipeline
            │   │   │   └── pipeline_config.json
            │   │   ├── study.json
            │   │   └── trials.tsv
            │   ├── radical_summary.tsv
            │   ├── sample_scoring.tsv
            │   ├── test.edgelist
            │   ├── train.edgelist
            │   ├── validation.edgelist
            │   └── weighted.edgelist
            └── 5
                ├── RotatE
                │   ├── cross_validation_results.json
                │   ├── embedding.tsv
                │   ├── pykeen_results_final
                │   │   ├── metadata.json
                │   │   └── results.json
                │   ├── pykeen_results_optim
                │   │   ├── best_pipeline
                │   │   │   └── pipeline_config.json
                │   │   ├── study.json
                │   │   └── trials.tsv
                │   ├── test.edgelist
                │   ├── train.edgelist
                │   └── validation.edgelist
                ├── cross_validation_results.json
                ├── embedding.tsv
                ├── network_summary.tsv
                ├── pykeen_results_final
                │   ├── metadata.json
                │   └── results.json
                ├── pykeen_results_optim
                │   ├── best_pipeline
                │   │   └── pipeline_config.json
                │   ├── study.json
                │   └── trials.tsv
                ├── radical_summary.tsv
                ├── sample_scoring.tsv
                ├── test.edgelist
                ├── train.edgelist
                ├── validation.edgelist
                └── weighted.edgelist
```

