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

> [!NOTE]
> ROCm does not currently support RX 6600 (gfx1032 or  10.3.2).
> in order to use GPU acceleration, it is possible to override the
> HSA to a similar supported version (gfx1030 or 10.3.0).

you may tweak it to use it with other GPUs (i.e NVidia) or your
CPU by following the [Ollama docs](https://docs.ollama.com/docker).

usage:

```bash
$ ollama-setup
```

### `anythingllm-setup`

this script sets up an AnythingLLM container via docker.

all that's needed to set up is provide the script a path that can
be used as AnythingLLM's permanent storage directory.

usage:

```bash
$ anythingllm-setup ~/.AnythingLLM
```

after that, you can open `localhost:3001` in your browser.
