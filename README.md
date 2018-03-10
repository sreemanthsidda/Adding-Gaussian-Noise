# Adding-Gaussian-Noise

I = imread('eight.tif');
J = imnoise(I,'gaussian', 0,0.02);
K = histeq(I);

figure, imshow(I);
figure, imshow(J);
imshowpair(I,K,'montage')
axis off
