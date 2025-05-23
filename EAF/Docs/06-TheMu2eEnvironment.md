# The Mu2e Python environment

To ensure that users have immediate access to the libraries and tools needed to conduct analysis, we have an installed a Mu2e Python environment on `/cvmfs`, called `mu2e_env`, that can used on **both** EAF and the virtual machines.

To set up this environment on EAF:

1. Create an environment symlink to the `current` version:
   ```bash
   ln -s /cvmfs/mu2e.opensciencegrid.org/env/ana/current ~/.conda/envs/mu2e_env
   ```

2. Activate the environment:
   ```bash
   mamba activate mu2e_env
   ```

## Available libraries in `v1.2.0`

- matplotlib
- pandas
- uproot
- scipy
- scikit-learn
- pytorch
- tensorflow
- jupyterlab
- notebook
- statsmodels
- awkward
- urllib3 (v1.26.16)
- ipykernel
- conda-pack
- fsspec-xrootd
- htop
- vector
- plotly
- dash
- anapytools (v2.0.0) 

## Use on the `gpvms`

To use `mu2e_env` on the Mu2e virtual machines:

```bash
# Activate
source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/activate

# Deactivate
source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/deactivate
```

Suggested aliases for `.my_bashrc`:

```bash
alias pystart="source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/activate"
alias pystop="source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/deactivate"
```

When using alongside `muse`:

```bash
mu2einit
muse setup ops
pystart # or source /cvmfs/mu2e.opensciencegrid.org/env/ana/current/bin/activate
```

Activate after `muse setup` to ensure that your environment variables are set correctly. 

## Interactive use 

`mu2e_env` also includes an in-built interactive kernel, also called `mu2e_env`. See the following exercise for more information! 

## Navigation

- Previous: [Using Conda/Mamba](05-CondaMamba.md)
- Next: [Exercise: "Hello world!"](07-HelloWorld.md)
- [Back to Main](../README.md)