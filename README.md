# pip-tools-bug-extra-repro
Reproduce bug with pip-tools when having an extra

## Setup

### (Optional) If you use pyenv

`pyenv virtualenv 3.9.1 pip-tools-bug-extra-repro`

### Install pip-tools

`pip install pip-tools`

## Test

Remove the `.txt` files and run `./pip-compile.sh` twice:

```bash
rm *.txt
./pip-compile.sh
git add .
./pip-compile.sh
git diff
```
