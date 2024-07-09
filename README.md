# Phonopy==2.20.0 image

Very early stage dev.

Phonopy can be found in `/opt/conda/bin/phonopy`. 
To build the image:

```shell
docker build . -t mikibonacci/phonopy-2.20.0:amd64 --platform linux/amd64
```

To use it with Appcontainer:

```shell
apptainer exec docker://mikibonacci/phonopy-2.20.0:amd64 phonopy
```

If the architecture is `arm64`, just change the `amd64` in the above command.