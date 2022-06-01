# installing python with conda

Go to https://docs.conda.io/en/latest/miniconda.html and find the correct installer for your system.

# setting up the conda environment

Following [napari](https://napari.org/)'s example, set up a virtual environment by opening your terminal (mac, linux) or opening
the anaconda prompt (windows).
### windows
<img src="https://user-images.githubusercontent.com/17855764/150007446-ca13db5a-423a-4351-bc85-aa49c78979f1.png" width="480">

Once in the terminal / command prompt, use the following lines to install the necessary packages.
```bash
conda create -y -n napari-env python=3.8
conda activate napari-env
pip install "napari[all]"
pip install wsireg
pip install napari-wsireg
pip install napari-imsmicrolink
```

# launching napari in your virtual environment

```bash
# activate environment
conda activate napari-env
# start napari
napari
```

Now `napari-imsmicrolink` should be available as a plugin in the napari plugin menu.

# running wsireg from the command line
Once you have set up your registration .yaml file (see [template](./reg-template.yaml)), you can run registration from the command line like so
```bash
conda activate napari-env
wsireg "path/to/my-reg-file.yaml"
```

