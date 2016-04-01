# NETS 213 final project

### Stratifying Twitter Social Spheres

Group members: John Hewitt, Roger Luo, Alice Ren

#### Data Collection (2 points)

In this phase, we will collect our data set from Twitter using the Twitter API, filtering out tweets from verified Twitter accounts (thus removing most tweets from corporations, celebrities, or other public figures who could skew our results). 

Milestones:
- Collect initial body of tweets
- Filter down to final data set to use

#### Crowdsourced Analysis (4 points)

Use a crowdsourcing platform (most likely Amazon Mechanical Turk) to collect answers from workers on the intended audiences and excluded audiences of tweets. We will ask each worker to choose from a predefined list of possible audiences, as well as enter a new label of their own for one possible intended audience and one excluded audience.

Milestones:
- Create and test the task interface, making sure it pulls tweets and collects answers appropriately
- Determine parameters for task (number of workers per task, cost per task) and run it until the desired number of results has been gathered

#### Aggregation of Results (3 points)

For questions with a constrained set of inputs, we will aggregate the results by simply counting up the number of votes for each answer and selecting the top two as the most likely correct answers. For the freeform inputs, we will simply store each unique input as a separate answer.

Milestones:
- Aggregate results for constrained-input answers
- Aggregate results for freeform-input answers

#### Quality Control (4 points)

For each tweet, we will ensure the quality of the constrained-input questions by creating a subsequent task that shows workers the tweet and the top two answers as determined in the previous tasks, then asks workers to choose the one that makes the most sense. 

We will control for the quality of the freeform-input questions by simply showing workers the tweet and user-generated label, and asking them whether or not it applies.

For both these tasks, we will also have a set of gold-standard "known" tweets and their appropriate answers.

Milestones:
- Create gold standard sets of tweets and audiences
- Create interface for quality control task and launch it
- Discard results that do not pass the quality control test

#### Training the Classifier (4 points)

Extract n-gram features from the labelled tweets and use them to train our social sphere tweet classifier. Siphon more tweets from Twitter for a test data set, then use our classifier to classify them. We will then manually evaluate the correctness of the tweet labels assigned by our classifier.

Milestones:
- Writing classifier
- Gathering the test data set
- Evaluating correctness of the classifier output
