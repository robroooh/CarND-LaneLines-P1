#**Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

My algorithm basically is that

    use HSV color space finding all lane lines
    group left/right lanes together
    filter out the line that its slope is too low
    for each side of lane lines do:
        finding the average slope & intercept, find ymax, find ymin
        given avg of slope&int, ymax,ymin - calculate new Xs
        plot the line accordingly

I can imagine possibilities of improving my algorithm here

    investigating on how to choose proper HSV value to get yellow&white color even in the tree shadow
    adjusting proper Hough parameters (trial&error)
    to construct the line as pieces of line, not the straight line, so that it is able to run on curvy lanes

Where my algorithm is likely to fail

    in sense of dynamic light& color
    shaky camera & camera is not centered
    at night
    curvy lane lines

