# 📈 Smart Strategies for an Effective Marketing Campaign 🚀

## 🌐 Background

Welcome to the digital heart of the modern era, where information flows boundlessly, and businesses continuously seek innovative ways to capture customer attention. "ClickStream," a budding enterprise in the competitive e-commerce space, grapples with the challenge of understanding its users to serve them better. Recognizing that an engaged customer is the linchpin of growth, ClickStream is keen to deploy smarter marketing strategies.

Until now, ClickStream has leaned on one-size-fits-all marketing tactics. But in a world where every click is gold, personalization is paramount. The firm has amassed a plethora of data regarding user interactions with their platform. Yet, without the application of data science, these digits remain just that – numbers.

Your role as a data scientist is pivotal. By deciphering user behavior patterns, you can assist ClickStream in transmuting this data into bespoke marketing stratagems. In doing so, you're not only bolstering sales but also enhancing the customer journey.

## 🗂️ Dataset

You'll be equipped with two detailed datasets, offering a deep dive into user interactions with the ClickStream platform.
`user_data.csv` - User Data

This set embodies user demographic and behavior details. Each row corresponds to a unique user.

`user_id`: The unique identifier for the user.

`age`: The user's age.

`abandoned_cart`: Whether the user has left a shopping cart without making a purchase (True/False).

`user_category`: User category based on their history (new_user, recurring_user, premium_subscriber).

`session_data.csv` - Session Data

This table delineates specifics about individual user browsing sessions. Each row represents a distinct session.

`user_id`: The unique user identifier for the user.

`session_id`: The unique session identifier.

`timestamp`: The date and time the session commenced.

`device_type`: Device type used (mobile, tablet, desktop).

`browser`: The web browser employed during the session.

`operating_system`: The device's operating system.

`ip_address`: The user device's IP address.

`country`: The country from which the session originated.

`search_query`: Search terms the user inputted on the website.

`page_views`: Number of pages viewed during the session.

`session_duration`: The session's total duration in seconds.

## 📊 Data Processing

During data processing, missing values should be handled, ensuring the dataset is complete and suitable for analysis. Participants are encouraged to user feature engineering techniques to derive new features and transform existing ones, enhancing the model's predictive power.

## 🤖 Model

You are at liberty to choose the classification algorithm. Whether it be a decision tree, random forest, or a more sophisticated ensemble or deep learning model, select the one that you believe will perform the best for this classification task.

## 📂 Repository Structure

The repository structure is provided and must be adhered to strictly:

```markdown
nuwe-data-ds1/
├── model.py
├── predictions
│   └── example_predictions.json
├── README.md
├── requirements.txt
├── test
│   ├── session_test.csv
│   └── user_test.csv
└── train
    ├── session_train.csv
    └── user_train.csv
```

-test/: Folder containing the user and session data for model validation. -train/: Folder containing the user and session data for model training

## 🎯 Tasks

You're tasked with concocting a predictive model that, harnessing user behavioral data, can pinpoint patterns and guide the marketing team in user segmentation for future campaigns. This segmentation will empower ClickStream to channel its resources more adroitly and craft messages that resonate with diverse user types.

As part of your responsibilities for the ClickStream challenge, you are expected to perform the following key tasks:

Task 1: Calculate the `marketing_target` Column. Utilize the provided datasets to compute and assign a `marketing_target` value for each user. This column should reflect the predicted engagement level of the user with the marketing campaign, with values assigned as follows:

`1` for Low engagement

`2` for Medium engagement

`3` for High engagement

Your calculated `marketing_target` values will be crucial for the subsequent segmentation and personalization of the marketing strategies. Ensure your predictions are as accurate as possible to facilitate effective user engagement.

## 📤 Submission

To carry out this challenge, we expect to obtain a file in json format whose name is `predictions.json`, where we will have as key the test_id, from the file user_test.csv and as value the prediction of the `marketing_target` column that has as values 1,2 and 3 (low, medium, high). predictions.json:

```markdown
{
    "target": {
        "297": 1,
        "11": 3,
        "67": 3,
        "54": 3,
        "156": 2,
        "290": 2,
        "193": 3,
        ...
  }
}
```

## 📊 Evaluation

As part of our commitment to providing a clear and consistent assessment of performance, this practice will be evaluated automatically using the F1 Score metric. The evaluation process will utilize the predictions.json file, which contains your model's predictions.

The F1 Score is a widely recognized statistical measure used in classification tests, which balances precision and recall. It is especially useful in scenarios where the distribution of class labels is uneven, providing a more nuanced insight into the model's predictive power.

Your predictions will be compared against the true values to calculate the precision and recall, from which the F1 Score will be derived. The closer your F1 Score is to 1, the better your model's performance is considered in terms of both accuracy and robustness.

## CHALLENGE BY

![NUWE](/nuwe-logo.jpg)

## Solution

### Environment Setup

```bash
python -V
# Output: Python 3.12.1
```

```bash
# create a environment named -> samba-ai
python -m venv marketing-ai
```

```bash
# activate the environment
source marketing-ai/bin/activate
```

```bash
# deactivate the virtual environment
deactivate
```

```bash
# create a Jupyter Notebook kernel
pip install jupyter ipykernel
```

```bash
# add the virtual environment as a kernel for the jupyter notebook
python -m ipykernel install --user --name=marketing-ai --display-name="Py3.12-marketing-ai"
```

```bash
# verify kernel installation
jupyter kernelspec list
```

```bash
# If needed
jupyter kernelspec uninstall marketing-ai
```

## Submitted by: Ashish Soni
