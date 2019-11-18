
1) install package by running:

$ pip install -r requirements.txt

##############################################
##############################################

2)install mujoco
See- https://github.com/openai/mujoco-py


##############################################
##############################################


3) run code: 

without Dagger-
$ python scripts/run_behavior_cloning.py --expert_policy_file policies/experts/Ant.pkl --env_name Ant-v2 --exp_name test_bc_ant --n_iter 1 --expert_data expert_data/expert_data_Ant-v2.pkl

with Dagger-
(NOTE: the --do_dagger flag, and the higher value for n_iter)
$ python scripts/run_behavior_cloning.py --expert_policy_file policies/experts/Ant.pkl --env_name Ant-v2 --exp_name test_dagger_ant --n_iter 10 --do_dagger --expert_data expert_data/expert_data_Ant-v2.pkl

##############################################

4) visualize saved tensorboard event file:

$ cd data/<your_log_dir>
$ tensorboard --logdir .

Then, navigate to shown url to see scalar summaries as plots (in 'scalar' tab), as well as videos (in 'images' tab)
