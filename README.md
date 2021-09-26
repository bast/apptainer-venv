# Python virtual environment on Singularity

How to fetch the image:
```
$ singularity pull https://github.com/bast/singularity-venv/releases/download/0.1.0/venv.sif
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

I have used this wonderful guide as starting point and inspiration:
https://github.com/singularityhub/singularity-deploy
