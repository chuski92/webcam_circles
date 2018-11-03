# webcam_circles
Circle detection from online webcam images

![Circle detection Hand](https://github.com/chuski92/webcam_circles/blob/master/images/circle.gif?raw=true)

That detector uses the Hough Transform to detect the circles in the image. ALthough Hough transform was initialy developed to find lines in a image it can be used to find circles.
The Hough transform returns three parameters: the center of the detected circle (a,b) and a radius of that circle (r). So with that you can position the circle into the image.

You can change some parameters to fine tune the results:

GAUSSIAN_BLUR_SIZE = 7;
GAUSSIAN_BLUR_SIGMA = 2;

With that parameters you can tune the blur effect, that can help you to better dettect the circles, but it can also make it so noisy.


CANNY_EDGE_TH = 150;

Edge detector threshold.

HOUGH_ACCUM_RESOLUTION = 2;

Resolution of the hough accumulator. 1 = same as the image, 2 = double size, etc.

MIN_CIRCLE_DIST = 40;

Minimum distance between circle centers.

HOUGH_ACCUM_TH = 70;

Threshold for the circle centers in the detection stage, the smaller it is, worst detection, it means more false circles it will detect.

Hough accumulated threshold.

MIN_RADIUS = 20;
MAX_RADIUS = 100;

Minimum and maximum radius of the detected circles, if detected circle has minus or more than that radius it will be not shown.

References:

[1] https://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/hough_lines/hough_lines.html
