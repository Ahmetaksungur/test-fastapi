Runpod üzerinde 80 port eklenmesi gerekli önce

git clone https://github.com/Ahmetaksungur/test-fastapi.git

cd test-fastapi

mkdir upload

pip install "fastapi[all]"

pip install --upgrade diffusers[torch]

pip install transformers

uvicorn main:app --host 0.0.0.0 --port 80^^

## Görüntüyü Siyah/Beyaz Yapma

```matlab
img1 = imread('test.jpg');
img1gri = rgb2gray(img1);
imshow(img1gri);
```
## Görüntüyü Döndürme

```matlab
img1=imread('test.jpg');
rotated_image = imrotate(img1, 30);
imshow(rotated_image);
```

```matlab
img1=imread('test.jpg');
size(img1);
[a,b,c]=size(img1);
```

## Resim Histogram

```matlab
img1=imread('test.jpg');
img1gri = rgb2gray(img1);
imhist(img1gri);
g = imadjust(img1gri, [0.5 0.9], [0.3 0.4]);
imshow(g);
figure, imshow(img1gri);
```

