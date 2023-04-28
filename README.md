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
## Resim Negatif Çevirme

```matlab
img1=imread('test.jpg');
img1gri = rgb2gray(img1);
n = imadjust(img1gri, [0 1], [1 0]);
figure, imshow(n);
neg = 255 - img1gri;
figure; subplot(1,2,1); imshow(img1gri); title('orjinal resim');
subplot(1,2,2); imshow(neg); title('negatif resim');
```
## Resmi Koyulaştirma ve Açma (intensity degisimi)

```matlab
img1=imread('test.jpg');
img1gri = rgb2gray(img1);
k = imadjust(img1gri, [], [], 1);  k1 = imadjust(img1gri, [], [], 4);
figure, imshow(k1);
figure, imshow(k);
```

## Resmi Logical yani binary'ye dondurme

```matlab
img1=imread('test.jpg');
img1gri = rgb2gray(img1);
d = im2bw(img1gri);
figure, imshow(img1gri);
```

## Resmin Buyuklugunu degistirme ve kaydetme

```matlab
img1=imread('test.jpg');
s = imresize(img1, [60 60]);
imwrite(s,'abc.jpg','Quality',100);
imwrite(s,'kayipsiz.jpg','Mode','lossless');
```

## Resmin Boyutunu Değiştirme ve Toplama

```matlab
img5 = imread('abc.jpg');
img6 = imread('test.jpg');
imshow(img5);
reimg5 = imresize(img5,[500 500]);
reimg6 = imresize(img6,[500 500]);
figure, imshow(reimg5);
t = reimg5+reimg6;
figure, imshow(t);
```

## İki Resmi Yan Yana Getirme

```matlab
img5 = imread('abc.jpg');
img6 = imread('test.jpg');
reimg5 = imresize(img5,[500 500]);
reimg6 = imresize(img6,[500 500]);
z(1:500, 1:500, :)=reimg5;
z(1:500, 501:1000, :)=reimg6;
imshow(uint8(z));
```
## İki resmi iç içe geçirme

```matlab
a = imread('abc.jpg');
b = imread('test.jpg');
a = imresize(a,[size(b,1), size(b,2)]);
imshow(a+b)
c=a+b;
a(1,1,1)
b(1,1,1)
c(1,1,1)
d=a*0.5+b*0.5;
figure, imshow(d)
```

## Resmin Kontrastini Degistirme / ussel donusum 

```matlab
I = imread('test.jpg');
Id = im2double(I);

output11 = 4*(((1+0.3).^(Id))-1);
output22 = 4*(((1+0.4).^(Id))-1);
output33 = 4*(((1+0.6).^(Id))-1);

subplot(2,2,1), imshow(I); title('Orjinal Resim');
subplot(2,2,2), imshow(output11); title('for 0.3');
subplot(2,2,3), imshow(output22); title('for 0.4');
subplot(2,2,4), imshow(output33); title('for 0.6');
```



