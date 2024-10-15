# Phonopy==2.20.0 image

Very early stage dev.

Phonopy can be found in `/opt/conda/bin/phonopy`. 
To build the image:

```shell
docker build . -t mikibonacci/phonopy-2.20.0:amd64 --platform linux/amd64
```

## To use phonopy just run:

````shell
docker run -it <image-name> phonopy # and the cmd line argument you usually use.
```

if you run without any other input arguments, you should obtain:

````shell
$docker run -it af2e94f769c6 phonopy
        _
  _ __ | |__   ___  _ __   ___   _ __  _   _
 | '_ \| '_ \ / _ \| '_ \ / _ \ | '_ \| | | |
 | |_) | | | | (_) | | | | (_) || |_) | |_| |
 | .__/|_| |_|\___/|_| |_|\___(_) .__/ \__, |
 |_|                            |_|    |___/
                                      2.20.0

Python version 3.12.2
Spglib version 2.5.0


Supercell matrix (DIM or --dim) was not explicitly specified.
By this reason, phonopy_yaml mode was invoked.
But "phonopy_params.yaml", "phonopy_disp.yaml" or "phonopy.yaml" could not be found.
  ___ _ __ _ __ ___  _ __
 / _ \ '__| '__/ _ \| '__|
|  __/ |  | | | (_) | |
 \___|_|  |_|  \___/|_|


```

## To use it with Appcontainer or singularity:

```shell
apptainer exec docker://mikibonacci/phonopy-2.20.0:amd64 phonopy
```

If the architecture is `arm64`, just change the `amd64` in the above command.

## docker hub images:

https://hub.docker.com/r/mikibonacci/phonopy-2.20.0/tags
