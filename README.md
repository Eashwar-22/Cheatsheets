# Setting up stuff

#### Best method to install tensorflow : https://www.youtube.com/watch?v=ykCY_tJbhNw
```

Step 1: download & extract tensorflow_macos--> https://github.com/apple/tensorflow_macos/releases/download/v0.1alpha3/tensorflow_macos-0.1alpha3.tar.gz

Step 2:
conda create -n new_env python=3.8. (3.8 is a must)
/Users/eashwar/Downloads/tensorflow_macos/install_venv.sh -p
(give env path) /Users/eashwar/miniforge3/envs/nlp
Click on y
Test --> python ---> import tensorflow
```


```
Another Method (not recommmended)
Startover - Install python, conda , tensorflow : https://github.com/mrdbourke/m1-machine-learning-test
Note : Ignore python -m pip install tensorflow-metal ---> throws error while importing tensorflow




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
