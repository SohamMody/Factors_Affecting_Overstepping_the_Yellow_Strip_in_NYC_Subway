# Factors Affecting Overstepping the Yellow Strip in the NYC Subway

I did this project along with Pranay Anchan for the course Urban Sensing as part of my Masters in Urban Data Science at New York University.

There are above 150 incidents annually of people being struck by trains in the NYC subway. There is a platform marked yellow near the entry point of the train in every station. This serves as a warning indicator and the authorities say that ‘standing on or at the yellow platform edge strip is dangerous'. We believe that the primary reason for these incidents is people overstepping onto this yellow platform, which puts them at potential risk of falling over and being struck by the train.

So, we decided to explore the factors involved that make the people do so using video and LIDAR sensors. As the project involved having to collect the data ourselves, we narrowed the scope of the project to just the R-line and the A-C-F line platforms of the Jay Street Metrotech station in downtown Brooklyn.

We suspected 2 major reasons for this overstepping:
1. People step onto the yellow platform due to the platform being overcrowded.
2. People step onto the yellow platform due to space-constrained subway platforms.

So, we chose to capture the video data for the morning rush hour and late night for non-peak hours for each of the platforms. The length of each video was around 20 minutes. Also, we scanned both the plaforms to get the design and spacing using the LIDAR sensor.

We used CloudCompare to analyze the LIDAR data and get the distances from that while we used OpenCV to process the video data and count the number of people crossing which were detected by a pre-trained Caffe object detection model. The steps taken by us for the LIDAR and video processing can be found in our [report](https://github.com/SohamMody/Factors_Influencing_Overstepping_the_Yellow_Strip_in_the_NYC_Subway/blob/master/Urban%20Sensing%20Project%20Report.pdf) uploaded to the repository. Also, the code for processing the video can be found [here](https://github.com/SohamMody/Factors_Influencing_Overstepping_the_Yellow_Strip_in_the_NYC_Subway/blob/master/people_counter.py). However, I have not uploaded the data to Github as the files were too large. Send me an email at sohamrmody@gmail.com if you are interested in it and I can give you access to the files.

After processing both the LIDAR and the video data, we were able to conclude that the platform size and the density of people on the platform does affect the choice of people to walk on the yellow platform. This is because we saw that the normalized count of people who overstepped onto the platform during rush hour on the R platform ,which is much narrower than the A-C-F, was much higher than the counts in the other scenarios. But, we cannot conclusively say that these might be the only reason for people to do so as we have noticed people doing it without any of these two reasons also.
