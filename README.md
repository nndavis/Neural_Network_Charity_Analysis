# Neural_Network_Charity_Analysis
 
## Overview
The purpose of this analysis is to create a binary classifier to predict whether or not applicants will be successful when funded by Alphabet Soup. The dataset contains over 34,000 organizations. To start, I had to preprocess the data for a neural network. Next was to compile, train, and evaluate the model. Lastly, was to optimize the model to the best of my ability. This was done in numerous ways that will be explained further in the results.

## Results
- Data Preprocessing
  - The target variable for the model is the "IS_SUCCESSUL" column.
  - The feature variables are "APPLICATION_TYPE", "CLASSIFICATION", "AFFILIATION", "INCOME_AMT", "USE_CASE", "ASK_AMT" and "SPECIAL_CONSIDERATION".
  - The variables that are neither targets nor features are "NAME" and "EIN".
  <img width="756" alt="image" src="https://user-images.githubusercontent.com/104074135/201191767-edf64c00-ef34-49d2-9a7e-58a0d92c39ae.png">
  
- Compiling, Training, and Evaluating the Model
  - I selected two dense layers, 8 neurons in one, 5 neurons for the other, and relu as my activation functions. I chose relu because it is closer to behaving linear, and is the most popular for training deep learning models. I used two dense layers with low neurons to make sure I wasn't overfitting the data at first. This number was bumped up during optimization, but failed regardless.
  - I was not able to achieve the target model performance.
  - I tried adding an additional layer. I raised my neurons significantly higher. I tried using tanh and sigmoid activations in conjuction on my first attempt. I also       raised my binning amounts to sort into less on my first attempt. For the first attempt I also tried lowering my features by dropping more columns. 
  
    <img width="634" alt="image" src="https://user-images.githubusercontent.com/104074135/201196029-5ce90d33-5bda-4822-b8fb-a671c9cc6456.png">
    <img width="599" alt="image" src="https://user-images.githubusercontent.com/104074135/201195511-5bcfd552-9fd8-4215-bc99-bbacbaab27eb.png">
    <img width="520" alt="image" src="https://user-images.githubusercontent.com/104074135/201195550-003dbba1-e4c8-478a-876d-d136cdfc2179.png">
    
    In the second attempt I lowered my binning amounts for more separation. I dropped only the "EIN" column. I changed all the activations back to relu. 
    
    <img width="511" alt="image" src="https://user-images.githubusercontent.com/104074135/201196233-95eef250-6e82-41fb-8856-01630aae06d1.png">
    <img width="344" alt="image" src="https://user-images.githubusercontent.com/104074135/201196282-705b9d16-f22a-4e4a-9fec-f5ab057b95a1.png">
    <img width="632" alt="image" src="https://user-images.githubusercontent.com/104074135/201196360-e3bfc00c-2a53-4137-bdf5-b30739fd2a1b.png">

    
    For the third attempt I tried changing one of my bins to bin "NAME" rather than application type. 
    
    <img width="512" alt="image" src="https://user-images.githubusercontent.com/104074135/201196623-8cc58736-af5d-4d0c-90c0-ca07c1ac6566.png">

    
    None of my attempts made any significant difference.
    
    ## Summary
    Overall the results were underwhelming. I was consistently getting around 0.69 loss and 0.53 accuracy. When I was overfitting with my layers and nodes the only difference was that it would take less epochs to achieve the same scores. The activation types did not make much of a difference. Nor did changing my bins really alter the end results. In my next attempt, I would add more bins rather than replace a current bin. This would be to remove rare occurences that are making me lose accuracy. If I could not get a neural network to work, I would try an unsupervised machine learning approach. 
