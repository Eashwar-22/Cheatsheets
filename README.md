# Setting up stuff

```
download tensorflow on mac m1:
1. create environment    ------> conda create -n tf tensorflow     (done)    
2. using tf on jupyter   ------>  conda activate tf
                                  conda install jupyter
                                  python -m ipykernel install --user --name=tf.   (done)
```

```
default conda env in terminal:

conda create -n my_env
conda config --set auto_activate_base true
conda activate base
cd ~
ls -a
vi .zhsrc   (if it is a zsh terminal)
press i to insert, enter "source activate my_env".  (without double qoutes) below <<conda initialize
press esc to leave insert mode and :wq to exit
source .zhsrc to make the config effective
close and reopen terminal, default my_env is activated


https://makeoptim.com/en/tool/conda-default-python-env
```
