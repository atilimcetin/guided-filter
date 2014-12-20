Guided filter for OpenCV
========================

Guided filter is an edge-preserving smoothing filter like the bilateral filter. Moreover, it's straightforward to implement and has O(n) complexity independent of the kernel size.


Examples
--------


```c++
cv::Mat I = cv::imread("./img_smoothing/cat.bmp", CV_LOAD_IMAGE_GRAYSCALE);
cv::Mat p = I;

int r = 4; // try r=2, 4, or 8
double eps = 0.2 * 0.2; // try eps=0.1^2, 0.2^2, 0.4^2

eps *= 255 * 255;

cv::Mat q = guidedFilter(I, p, r, eps);
```




License
-------

MIT license.

