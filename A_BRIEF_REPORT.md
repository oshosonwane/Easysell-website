So 1st lets see what methodologies and approches i tried. This code uses topography to solve the matching probllem like firstly i made creted cam_1 and cam_2 to 
Save all info about the players tracked by the yolo model saved it in different files, then checked the frame where there is a suddent jup for broadcast vedio by
checking the no of players per frame then then to alighn them i chopped 3 seconds from tractcam vedio updated cam_2 to cam_2_synch file then just did toplogical
matching using  voting and remove matches for vote less than 10 then simply lables with different colours and created a vedio final_solution.mp4 .




For techniques, my first try was homography matching, like I tried everything, direct homography matching (separate for wide and close shots, which i distinguised 
using the technique described earlier, I tried getting homography for both videos h1,h2, such that we get top-down homography. I even added the top-to-bottom frame of 
the stadium, and so I took like a football template, did SIFT matching RANSAC to get the homography, but the issue was that they needed at least 4 points  to get a 
perfect homography, so yaa it didn't work tbh i am still working on it so yaa 


challanges biggest challange was the close up shots this is also like my incomplete part i was thinking like take the frame just before the is a jump in broadcast 
vedio and for just one frame do a feature or any kind of matching of player in close up shot to shot in tractcam vesio idk why its not working at at all like there 
are many issuesss coming up like i improved the sinc  to get bettert result i notices in close up shots it was tracking the shoes so i expanded the box size so that
matching will be better(it did it only fot he broadcast vedio only for expanded frames) got bettetr reslut still i thik there is some issue in topography ids and how
i am saving it in file i will look into it i think this logic of frame matching sotn have theriotical flaw atleast on paper but let see 

