# clickPOILabeler
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/b243ea298aaf4a0f9a7e87378a7e6d93)](https://www.codacy.com/app/igponce/click-labeler?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=igponce/click-labeler&amp;utm_campaign=Badge_Grade)

Point-and-click POI labeler for images (needed before you want to train an algorithm or neural network)

So you want to train a neural network, and you have enough images. Great.
Problem is you need to label some features present in the images in order to train the algorithm... and that's not as easy as it sounds.

## Prerequisites

* Python3
* numPy
* openCV3

## How to use

```{bash}
click_labeler.py <image to label>.{png|jpg}
```

![Just click where you want the feature to label](click_feature.jpg)


### Keys

To reset the points press 'r'.
To save changes press 's' or 'x' (save, exit).
To exit, press q.

If you try to save changes withot clicking any point, the program will end.

### Use in directories

If you want to use the program to label *every* file in your directory, use the shell:

 ```{bash}
 for i in /path/to/directory/with/a/huge/amount/of/files.jpg ; do
    click_labeler.py -i $i
 done
 ```
 
### Output
The program will write a file with the same name as the image file with the "points".
This is a pipe-separated text file with the X, y coordinates ( from (0,0) on the top left corner to (1,1) on the bottom right) of each point.




