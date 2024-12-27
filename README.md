# Reproduction of experiments

## Install PyPy inside conda env
```shell
conda create -c conda-forge -n my-pypy-env pypy python=3.9
conda activate my-pypy-env
```

## Install requirements (suggested to run in a new virtual environment)

```shell
pip install -r requirements.txt
```


## Test FIFO and CR dispatching startegies

```shell
./reproduce_dispatcher_experiments.sh
```

**Known issue:** Reference data (`datasets/[lots/machines]_SMT2020_[HVLM/LVHM].txt`) required for evaluation is not available - impacted code in `eval_results.py` has been commented out. Output file `greedy/_greedy_sum.txt` will not have reference stats/benchmark for comparison.

## Dataset

Our simulator uses the SMT2020 dataset. It is available on https://p2schedgen.fernuni-hagen.de/index.php/downloads/simulation

Kopp, Denny & Hassoun, Michael & Kalir, Adar & Mönch, Lars. (2020). SMT2020—A Semiconductor Manufacturing Testbed. IEEE Transactions on Semiconductor Manufacturing. PP. 1-1. 10.1109/TSM.2020.3001933. 

