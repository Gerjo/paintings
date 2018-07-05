# Renaisance era painting dataset with annotated hands and faces
These paintings and annotations are used in my MSc project on the subject of using algorithms to automatically detect hands in Renaissance era paintings.

The images and some meta data are sourced from [WikiArt.org](https://www.wikiart.org/), whom employ a fair use principle. Hand and face annotations are manually added by me, and are hereby released under the CC BY 4.0 license for you to use.

# Annotation syntax
The annotations.xml file in this repository contains the following information:
 - <filename> Filename of the painting, relative to this repository;
 - <width> <height> The dimensions of the image;
 - <title> <author> <genre> <technique> <keywords> Meta data as provided by WikiArt;
 - <url> The original URL used to download the meta data from. Some URLs may no longer work as WikiArt updates its database;
 - <faces> <hands> Annotated data provided by me, with the following properties:
   - <x> <y> The center of the annotation rectangle. This is relative to the center of the painting. (i.e., some coordinates will be negative);
   - <w> <h> The width and height of the rectangular annotation;
   - <person> A unique number within a painting referring to a person. Note that these numbers are not necessarily incremental (During the annotation process I used colors to indicate persons, each color has a unique number);
   - <left> <right> A boolean indicating whether this pertains a left hand or right hand. This data is not available for faces. Note that some annotations are both left and right hands, this means hands of a single person are significantly overlapping and creating two overlapping annotations would've been too tedious. 

Only paintings with fewer than 5 persons are included. Paintings with too small hands are filtered.

# Why Renaissance era paintings?
An all too often asked question.
- Fun subject matter;
- All algorithms are also applicable to other domains (e.g., Renaissance hands look not too dissimilar from your hands - contrary to, say, Cubism hands); 
- I had never really worked with Computer Vision algorithms before;
- There appears to be no published work doing the same;
- Challenging dataset with generally noisy images and a reduced variance of colors (e.g., hardly any blue! and loads of red everywhere); 

# Examples of annotated hands
![image of some annotated hands](https://github.com/Gerjo/paintings/blob/master/example_hands.png?raw=true)

# Examples of annotated faces
![image of some annotated faces](https://github.com/Gerjo/paintings/blob/master/example_faces.png?raw=true)

