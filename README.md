# !MDP Playground

# To install all requirements:
conda env create -n <env_name> -f py36_toy_rl.yml
conda activate <env_name>
git clone https://github.com/anonips/-MDP-Playground.git
cd -MDP-Playground
pip install -e .
git clone https://github.com/anonips/Gym-Extension.git
cd Gym-Extension
pip install -e .

The file -MDP-Playground/rl_toy/envs/rl_toy_env.py contains the code for the Environments. It can be run as python rl_toy_env.py to instantiate Environments and run a random agent on them.

The file run_experiments.py has the run for the DQN experiments in the paper. It can be run as "python3 run_experiments.py <full path to CSV filename to save stats to>". It will save stats to 2 CSV files, with the filenames as the one given as argument to the experiments python script and another file with an extra "_eval" in the filename that contains evaluation stats during the training. These can be plotted using the plot_experiments.ipynb Jupyter Notebook.

Additional experiments can be run by changing the configurations within the run_experiments.py file.
