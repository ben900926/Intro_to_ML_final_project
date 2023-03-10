# NYCU Intro to ML final project

This repository is the official implementation of 2022 NYCU intro to ML final project by 109550146 劉沛凡

## Requirements

Note: Please use Python **3.8.15** version

To install requirements, please run my ipynb file in either:

 - **google colab**: modify the first cell to the following (**recommended**)

````
# download dependancy
!pip install optuna
!pip install category_encoders
````

>📋  Please use the latest version of Google Colab and run the first cell



 - **local (vscode)**:  Run the commands below in the first cell
 
 > *Note:* If you use Anaconda enviornment to run, make sure you install "ipykernel" by executing the following command:
 > ```
 > conda install -n <your env name> ipykernel --update-deps --force-reinstall
 > ```
 
 109550146_Final_train.ipynb and 109550146_Final_inference.ipynb
 
 ````
%pip install -r requirements.txt
 ````
 
 You can comment and uncomment out the part you needed in the first cell:
 ![image](https://user-images.githubusercontent.com/71249897/211455336-85589388-1049-4c6c-b15c-70519d434874.png)

 
 
After executing, you should see the following files (dont_click_me.csv, final_mdoel.pkl, test.csv, train.csv) show up on the left panel:

![image](https://user-images.githubusercontent.com/71249897/211157859-c5fd9aa7-a382-4ccc-b151-6212182acf13.png)


## Link to My Model

You can download pretrained models here:

- [My logistic regression model](https://drive.google.com/file/d/1-5d3PfMkJr7ln3xu5xQbZQsqlqqInJbq/view?usp=share_link) trained using parameter search.

## Reproducing Submission
To reproduce my submission, follow the steps below:

*Note: Please download my ipynb code and open it on VScode or Google Colab. **Don't open it directly in Github.***

1. Run 109550146_Final_train.ipynb (You can skip this if you use the model I provided above)
2. Run 109550146_Final_inference.ipynb
3. Following "SUBMISSION_PATH" to download my **109550146_submission.csv** file. By default, it can be found in the same directory as my ipynb file:
4. Submit it to Kaggle
![image](https://user-images.githubusercontent.com/71249897/211044969-2a4fe7a4-742b-4f5b-b136-745f36ca603e.png)


## Training

To train the model, run 109550146_Final_train.ipynb. Remember to execute all cells in order!

![image](https://user-images.githubusercontent.com/71249897/211019181-359e42a6-29c7-44ec-86eb-3d8c9ac52bea.png)

There are two parameters you should note while running my training code

 - MODEL_WEIGHT_PATH: This is where the code would store the weight of trained model. 
 The default path (drive/MyDrive/ml_final/model/final_model.pkl) is the path in my drive storing the weight file I provided. 
 **You should change the path to your own.**
 You can find this file following the link in the "Pre-trained Models" section.

 - PARA_SEARCH: This is to determine whether the parameter search is enabled. Default is set to "False", so that the best parameter I found is used. 
  If you want to take a look of how I do parameter search, you can enable it, but the result model might be different than the one I used for this project.

## Evaluation

To evaluate my model, run 109550146_Final_inference.ipynb in Google Colab. All cell should be executed in order.

**Note**: You should change the path to the model weight if you want to offer a new file to it.

![image](https://user-images.githubusercontent.com/71249897/211022420-a1064cd8-7e1e-4144-b147-25ca948992d6.png)

By default, my model weight is automatically downloaded to Google Colab in the first cell, 
so you don't have to change anything if you want to use the model I provided.

Also, the submission file is stored in SUBMISSION_PATH, so by default you should see **"109550146_submission.csv"** by clicking this button in left.

![image](https://user-images.githubusercontent.com/71249897/211044988-6a440380-ff8e-4477-aea6-9a9af102551b.png)

You can change the path if you want to store it in your drive.


## Results

My model achieves the following performance on :

### [Tabular Playground Series - Aug 2022 on Kaggle](https://www.kaggle.com/competitions/tabular-playground-series-aug-2022/leaderboard)

| Model name                      | Private Score       | Public Score       |
| --------------------------------|-------------------- | ------------------ |
| My logisitic regression Model   |     59.072%         |      59.014%       |

