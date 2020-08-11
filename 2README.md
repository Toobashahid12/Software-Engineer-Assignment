
Title And Authors ;

UI Screens Identification and Extraction from Mobile Programming Screencasts

“Conference icpc-2020 Program”

Authors Name:- 

(1) Mohammad Alahmadi

(2) Abdulkarim Khormi

(3) Sonia Haiduc

Introduction And Motivation:- 

Smartphones are some of the most widely used devices today, with more than 2.5 billion users worldwide. The two most popular app stores, the Apple App Store1 and Google Play Store2 host millions of smartphone applications that people use for a variety of tasks in their daily lives. When learning about new concepts and technologies, debugging, or looking for answers to programming questions, online resources are developers preferred documentation sources [9]. Screencasts are particularly on the rise, with tens of millions of videos available on many programming topics, hosted on platforms like YouTube. Screencasts can be effective learning tools for mobile app developers due to their ability to offer in-depth, step-by-step explanations on a particular programming topic and the fact that they show the mobile apps and their features in action. However, it can be often hard to find a screencast that addresses the topics, features, or app elements for which a developer might be searching for. Our approach for extracting the UI overview, called UIScreens, is based on a deep Convolutional Neural Network (CNN) which includes an image feature extractor and an object detector to locate UI screens within the frames of a programming screencast. The detected UI screens are then extracted and filtered such that only unique UI screens are kept.

Research And Methodology:- 

Research Qno1= 

How accurate is our approach at classifying UI frames and locating UI screens in mobile programming screencasts?

Research Qno2= 

To what extent are the extracted UI screens considered unique and sufficient by developers?
We trained our approach as described in Section 3 on the 4,000 UI and NonUI frames and their locations. We performed 10-fold cross-validation, where we split the data in each fold into training, validation, and testing sets. The validation and testing sets are each 10% of the data, while the training set is represented by the remaining 80% of the dataset. The validation dataset is used during the training to avoid overfitting. Our training process involved 4,000 iterations, until the network stopped improving and the validation loss was stable. The study was conducted through an online survey composed of two main sections. The first section was designed to capture demographic data, such as the main occupation (professional developer, academic, student) and the mobile programming experience (iOS and/or Android and number of years) of our participants. Each participant was required to have at least 6 months experience in at least one of the two mobile programming platforms to be qualified for participating in our survey. The study participants were recruited through announcements on professional social media channels. (“The list of UI screens extracted is sufficient to understand what are the main concepts discussed in the video”) and the second one referred to their uniqueness (“The list of UI screens extracted does not present duplicate information, i.e., all UI screens presented are unique”).

Results:- 

Ans RQ no1 =  We used different metrics for each of the classification and localization tasks. First, to evaluate the binary classification of the video frames into UI and NonUI, we used the standard metrics of Precision, Recall, F1 score, and Accuracy. We denote Tp as the number of true positives, Tn as the number of true negatives, Fp as the number of false positives, and Fn as the number of false negatives. Precision is then defined as P = Tp Tp+Fp and Recall is computed as R = Tp Tp+Fn . The F1 score is the harmonic mean of precision and recall, defined as F1 = 2 · P ·R P+R . Accuracy represents the percentage of correctly classified instances and is formally defined as Acc = Tp+Tn Tp+Tn+Fp+Fn . To evaluate the task of locating UI screens within the UI frames, we used the Intersection over Union (IoU) metric between the predicted location and the ground truth location.
Ans RQ no2= In 85% of their responses, developers either weakly or strongly agreed that the UI screens extracted by our approach were sufficient in understanding what the main elements discussed in the video were. At the same time, 83% of responses either weakly or strongly agreed that the extracted UI screens were unique when compared to each other. This indicates that UIScreens can efficiently extract distinct and sufficient UI screens in order to provide comprehensive UI overviews for mobile programming screencasts. Only 2% of the participants indicated that seeing a UI overview of a mobile programming screencast is not useful for any purpose. In total, 68% of the participants indicated that the extracted UI overview can help them understand if the video contains UI design or not, 66% thought the UI screens can help them understand the relevance of a video for their search needs, and 64% said the UI screens help them understand the main points of the video.

Conclusion:-

In this paper, we proposed a novel approach, called UIScreens, to locate and extract UI screens embedded in mobile programming screencasts, with the purpose of offering developers a UI-focused overview of a video. We conducted two evaluation studies to assess our approach in terms of its accuracy, and the quality and usefulness of its results. The evaluation showed that UIScreens was able to accurately classify and locate UIs in video frames. Additionally, UIScreens received positive feedback from mobile developers, showing potential for our approach to help developers in navigating and understanding the contents of mobile programming screencasts.
