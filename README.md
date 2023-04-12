pip install "fastapi[all]"

pip install --upgrade diffusers[torch]

pip install transformers

uvicorn main:app --host 0.0.0.0 --port 80
