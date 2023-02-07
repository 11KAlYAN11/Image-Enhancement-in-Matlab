# Image-Enhancement-in-Matlab
different techniques to improve the image brightness using brightness adoption techniques 


%%%%%%%%%%%%%%%matlab code%%%%%%%%%%%%%

% Read in image
img = imread('image.png');

% Convert image to double precision for processing
img = double(img);

% Define brightness factor (a value between 0 and 1)
b = 0.5;

% Apply nonlinear logarithmic remapping
img = log10(1 + b * img);
img = img / max(img(:));

% Convert image back to uint8 for display
img = uint8(255 * img);

% Show the processed image
imshow(img);

