# Fast Python virtual environments on [Apptainer](https://apptainer.org/)

I use it to install dependencies that may be tough to install on my NixOS environment.

How to fetch the image:
```
$ apptainer pull https://github.com/bast/apptainer-venv/releases/download/0.5.0/venv.sif
```


## Usage

- Reads: `requirements.txt`
- Creates: `venv` (folder)

Run `myscript.py` inside the virtual environment defined by `requirements.txt`:
```
$ ./venv.sif python myscript.py
```

Open python shell inside the virtual environment defined by `requirements.txt`:
```
$ ./venv.sif python
```


## Acknowledgements

- To build the image, I have used
  [this wonderful guide](https://github.com/singularityhub/singularity-deploy) as starting
  point and inspiration.
- Under the hood, the image uses Astral's [uv](https://astral.sh/blog/uv) to install
  dependencies.
