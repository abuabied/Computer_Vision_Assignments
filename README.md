# Computer_Vision_Assignments


Puzzle solver Project:
-Goal: Given a number of seperated puzzle pieces, we are required to construct the whole 
puzzle as accurate as possible, with using as many pieces as we can from the given pieces.

-Arguments: Puzzle pieces (some pieces are partially similar which helps assembling the puzzle),
correct place of the first piece.

-Method: Calculate the transformation matrix that maps the first piece to it's correct place,
then use SIFTING (discriptions & detection) to find other pieces with similar parts, 
then calculate the needed transformation that maps these parts to the correct place,
which leads to the piece itself being mapped to it's correct place.
Reapeat the proccess untill all pieces are used or no more matches found.

Photometric Stereo based View Synthesis:
-Goal: Generate a series of synthesized images, that represent a scene from different POVs.

-Arguments: Intrinsics of the used camera, 2 images taken by that camera with only horizontal 
10cm diffrence (same baseline).

-Method: Calculate the census-tranform for each image, then calculate the disparity. (use 
winner-takes-all approach after aggregation on the cost-volume, filter matches with simple 
consistency check). Calculate the depth of the left image, then use modified camera intrinsic so 
generate the synthesized image to it's right with 1cm horizantel difference.(change the intrinsics
by changing the x position of the camera). 
