# Adding-Gaussian-Noise and Salt and Pepper

I = imread('eight.tif');
J = imnoise(I,'gaussian', 0,0.02);
K = histeq(I);
L = imnoise(I,'salt & pepper',0.05);
M = histeq(L);
figure, imshow(I);
figure, imshow(J);
figure, imshow(M);
imshowpair(I,K,'montage')
axis off
