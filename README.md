# Vehicle Type Identification
As the demand for sustainable energy increased in the past few years, electrical vehicle had gradually replaced normal vehicle to reduce the carbon emission due to diesel burning by the normal vehicle. Charging stations for electrical vehicles had become another problem for shopping malls. In order to more accurately optimise the number of charging stations needed in the parking lot, the number of electrical vehicles enter the shopping malls must be identified through counting. However, due to their high similarity, it is not easy to differentiate between the electrical and normal vehicles through human counting. Thus, a system must be implemented for better identification.

In this section, the image classification of electrical and non-electrical vehivles was done by using transfer learning from a pre-trained network. The pre-trained model which served as the convolutional base provided a short pathway towards image classification as it had been previously trained with a large generic dataset. The pre-trained model could be used in multiple types of image classification problems as it had been trained to have a 'worldwide' vision. Herein, the model, 'MobilNet' was used as the convolutional base for transfer learning (Marcelino, 2018). 

The dataset collected was diverse, in which multiple brands of EV and non-EV images were processed to minimize biasness. However, to better fit the model for the use in Malaysia, a market survey was done to understand the EV markets in Malaysia, it was found that only around 500 EVs were currently on the road with very few brands available (Hans, 2021). Brands such as Nissan, Porsche, Renault, Mitsubishi, BMW, Tesla, MINI and Hyundai were among the top of the list. After careful consideration, only EVs manufactured by Nissan, Porsche, Renault, Mitsubishi, BMW and Tesla were chosen as the training data set.

After that, the method for data collection was discussed. In order to facilitate the recognition of EV by our model, the team had looked up for differences between EV and non-EV in terms of appearance. Then, it was realised that the EVs generally had smaller front grills as compared to non-EVs, thus front view images of vehicles were one of the focus for image collection. Then, another finding was the existence of exhaust pipe. Almost all non-EVs had an exhaust pipe at the back of them while it would not be always true for EVs. Thus, back view images of vehicles were the second focus for image collection. Lastly, it was also found that bottom views of the vehicle could be used as a potential data source for recognition due to the allignment of battery. In EVs, battery would be installed at the bottom thus a flat dark plate would be observed from the bottom view but mechanical parts would be observed if it were a non-EV. However, due to the lack of data for bottom views, this was not adopted at the end. Therefore, only front and back views of vehicles were collected for learning. Examples were shown below.


Front            |  Back
:-------------------------:|:-------------------------:
![image](https://user-images.githubusercontent.com/69382649/145414853-28d2ad0c-d2b0-4df0-8855-82a597e6bff4.png)  |  ![image](https://user-images.githubusercontent.com/69382649/145414761-0d3ff5e2-4032-4a49-92e9-857bd9faafd6.png)

About 45 images of EV and 45 images of non-EV from each brand were collected with equal front and back views. This made up a dataset of about 490 images. Then, the mixed dataset was splitted into two portion, in which the about 60% of the dataset was used as test set while the remaining portion was used as validation test set. 

To verify the result, the accuracy and loss of both test and validation test set were plotted.

## Reference
1. Marcelino, P. (2018, October 23). Transfer learning from pre-trained models - Towards Data Science. Medium. https://towardsdatascience.com/transfer-learning-from-pre-trained-models-f2393f124751
2. H. (2021, December 6). How many EVs are there on Malaysia roads? Slightly under 500, which brand leads? WapCar. https://www.wapcar.my/news/how-many-evs-are-there-on-malaysia-roads-slightly-under-500-which-brand-leads-31398
