Autonomous driving is one of the very complex technologies that is highly in demand. But safety will always be the top priority (both for the person inside the vehicle and people in the street) as accidents do not come along with a warning. Here, in this project our main objective is to predict the behaviour of a person on whether that person is going to cross the road or not. For the data collection, 62 videos were captured out of which 60 videos were for training and 2 videos were for testing. The videos were of two types, one being a person standing and not crossing the road and other one where the person is crossing the road. Based on these data, two sequential models (1. LSTM, 2.GRU) have been used to predict the crossing behaviour of test samples (one being crossing and the other being not crossing). 
The training dataset was generated from the training videos using OpenCV (developed by Intel) and MediaPipe library (developed by Google). Each video is composed of multiple frames where each frame generated 33 pairs of pose points by MediaPipe. The frames were labelled manually as 0 (when the person is not crossing) and 1 (when the person is crossing). For training the model, a sequence length of 15 was taken and the dataset was modified by shifting frames one by one in a sliding window fashion. The trained model was then used to predict whether a person is about to cross the road or not. 
Then we used this dataset for LSTM and GRU models to predict whether a person is going to cross or not based on probability values.
