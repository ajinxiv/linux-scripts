# ollama-docker

a few useful scripts to use ollama under a docker container

## usage


### `ollama`

this script is a wrapper that allows you to use ollama as if
it was installed directly on your computer, like this:

```bash
$ ollama -v
```

instead of this:

```bash
$ docker exec -it ollama ollama -v
```

> TIP: it also starts your ollama container if it is stopped.

### `ollama-setup`

this script sets up ollama via docker for AMD GPUs (ROCm).

you may tweak it to use it with other GPUs (i.e NVidia) or your
CPU by following the [Ollama docs](https://docs.ollama.com/docker).

usage:

```bash
$ ollama-setup
```
