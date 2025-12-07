## setup

```
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.lock
pip freeze >| requirements.lock
deactivate

rm -rf .venv
```
