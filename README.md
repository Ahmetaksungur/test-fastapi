Runpod üzerinde 80 port eklenmesi gerekli önce

git clone https://github.com/Ahmetaksungur/test-fastapi.git

cd test-fastapi

mkdir upload

pip install "fastapi[all]"

pip install --upgrade diffusers[torch]

pip install transformers

uvicorn main:app --host 0.0.0.0 --port 80

```matlab
imread('test.jpg');
img1 = imread('test.jpg');
img1gri = rgb2gray(img1);
imshow(img1gri);
```
