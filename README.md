# Embark_P4_T2
In this section, the image classification of electrical and non-electrical vehivles was done by using transfer learning from a pre-trained network. The pre-trained model which served as the convolutional base provided a short pathway towards image classification as it had been previously trained with a large generic dataset. The pre-trained model could be used in multiple types of image classification problems as it had been trained to have a 'worldwide' vision. Herein, the model, 'MobilNet' was used as the convolutional base for transfer learning. 

The dataset collected was diverse, in which multiple brands of EV and non-EV images were processed to minimize biasness. However, to better fit the model for the use in Malaysia, a market survey was done to understand the EV markets in Malaysia, it was found that only around 500 EVs were currently on the road with very few brands available. Brands such as Nissan, Porsche, Renault, Mitsubishi, BMW, Tesla, MINI and Hyundai were among the top of the list. After careful consideration, only EVs manufactured by Nissan, Porsche, Renault, Mitsubishi, BMW and Tesla were chosen as the training data set.

After that, the method for data collection was discussed. In order to facilitate the recognition of EV by our model, the team had looked up for differences between EV and non-EV in terms of appearance. Then, it was realised that the EVs generally had smaller front grills as compared to non-EVs, thus front view images of vehicles were one of the focus for image collection. Then, another finding was the existence of exhaust pipe. Almost all non-EVs had an exhaust pipe at the back of them while it would not be always true for EVs. Thus, back view images of vehicles were the second focus for image collection. Lastly, it was also found that bottom views of the vehicle could be used as a potential data source for recognition due to the allignment of battery. In EVs, battery would be installed at the bottom thus a flat dark plate would be observed from the bottom view but mechanical parts would be observed if it were a non-EV. However, due to the lack of data for bottom views, this was not adopted at the end. Therefore, only front and back views of vehicles were collected for learning. Examples were shown below.

![image](https://user-images.githubusercontent.com/69382649/145409368-3789863d-19a0-48c0-ae97-bd31f9a284bd.png)
<Front view>
  
![image](https://user-images.githubusercontent.com/69382649/145409000-6a3819ff-2133-4beb-9cd2-79c4639a0ec5.png)
<Back view>


About 45 images of EV and 45 images of non-EV from each brand were collected with equal front and back views. This made up a dataset of about 490 images. Then, the mixed dataset was splitted into two portion, in which the about 60% of the dataset was used as test set while the remaining portion was used as validation test set. 

To verify the result, the accuracy and loss of both test and validation test set were plotted.
