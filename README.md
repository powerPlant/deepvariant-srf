## Singularity recipe files for Deepvariant

https://github.com/google/deepvariant

Generate symlinks for executables
```
singularity exec deepvariant.1.4.0.sif find /opt/deepvariant/bin -type f -executable -printf "%f\n" | xargs -L1 ln -s deepvariant.1.4.0.sif
```

## GPU support
Set `SINGULARITY_NV=true` to enable GPU support where required. Useful in environment modules, like,

```
# Required to enable GPU
setenv SINGULARITY_NV true
```

