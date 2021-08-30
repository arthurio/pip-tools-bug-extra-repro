# pip-tools-bug-extra-repro
Reproduce bug with pip-tools when having an extra

## Setup

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
