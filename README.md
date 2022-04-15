# building a singularity container for crYOLO using CUDA version 11

Tru <tru@pasteur.fr>

## Why ?
- toy system for github actions
- build singularity container from dockerhub registry and push to oras://ghcr.io with proper tags 
- 
## Caveat
- playground, use at your own risk!
- `:latest` tagged singularity image

## Usage

- Singularity [![Singularity build](https://github.com/truatpasteurdotfr/singularity-cryolo-cuda11/actions/workflows/singularity-publish.yml/badge.svg)](https://github.com/truatpasteurdotfr/singularity-cryolo-cuda11/actions/workflows/singularity-publish.yml)
```
singularity run -B /run --nv  oras://ghcr.io/truatpasteurdotfr/singularity-cryolo-cuda11:latest
```

LICENSE:
The same as crYOLO (free for academic use, see https://cryolo.readthedocs.io/en/stable/other/license.html)
copy retrieved from https://raw.githubusercontent.com/MPI-Dortmund/cryolo/9ea47f694fc68bcdaedf550a128558b8e77855bc/source/other/license.rst
