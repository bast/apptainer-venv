# Python virtual environment on [Apptainer](https://apptainer.org/)

I use it to install dependencies that may be tough to install on my NixOS environment.

How to fetch the image:
```
$ apptainer pull https://github.com/bast/apptainer-venv/releases/download/0.4.0/venv.sif
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

---

To build the image, I have used [this wonderful
guide](https://github.com/singularityhub/singularity-deploy) as starting point
and inspiration.
