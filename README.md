# python_environments

Backup of Conda Python environments

To generate a backup environment file for all Conda environments, use:

```
conda env list| awk {'print $1'} | xargs -n 1 sh -c 'conda env export -n $1 -f $1.yml' argv0
```

To recreate any environment use:

```
conda env create -f environment.yml
```
