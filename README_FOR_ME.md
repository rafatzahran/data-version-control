# Data Version Control Tutorial


### Download Anaconda command line installer and install it
```console
shasum -a 256 ~/Downloads/Anaconda3-2021.11-MacOSX-x86_64.sh
bash ~/Downloads/Anaconda3-2020.02-MacOSX-x86_64.sh
bash Anaconda3-2021.11-MacOSX-x86_64.sh
```

### Create and activate a virtual environment (dvc)
```console
conda create --name dvc python=3.8.2 -y
conda init bash # NB! Close and open the terminal after this command
conda activate dvc
```

### Install libraries
```console
conda config --add channels conda-forge
conda install dvc scikit-learn scikit-image pandas numpy
```

### Fork and clone source code
```console
cd Documents/GitHub/
git clone https://github.com/rafatzahran/data-version-control.git
cd data-version-control/
```

### Download imagenette
- Go to the Imagenette [GitHub](https://github.com/fastai/imagenette) page and click 160 px download in the README.
- Copy the train/ and val/ folders and put them into your new repository, in the data/raw/ folder. 

### Practice the Basic DVC Workflow
1. To start, create a branch for your first experiment:
```console
git checkout -b "first_experiment"
```

2. Initialize DVC:
```console
dvc init
```
This will create a .dvc folder that holds configuration information.

**Note:** DVC has recently started collecting anonymized usage analytics so the authors can better understand how DVC is used. 
This helps them improve the tool. You can turn it off by setting the analytics configuration option to false:

```console
dvc config core.analytics false
```

3. Tell DVC where the remote storage is: 
You need some kind of remote storage for the data and model files controlled by DVC. 
This can be as simple as another folder on your system. Create a folder somewhere on your system outside the data-version-control/ repository and call it dvc_remote.

Now come back to your data-version-control/ repository and tell DVC where the remote storage is on your system:
```console
dvc remote add -d remote_storage /Users/raafatzahran/Documents/dvc_remote
```
Your repository is now initialized and ready for work. You’ll cover three basic actions:

- Tracking files
- Uploading files
- Downloading files

### Tracking Files
Add the train/ and val/ folders to DVC control:
```console
dvc add data/raw/train
dvc add data/raw/val
```

```console

```

```console

```

```console

```