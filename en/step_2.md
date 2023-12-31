## Create your machine learning model

Imagine you're trying to cut down on hotdogs and eat more healthily. This detector can help keep you on track by alerting you whenever a sneaky hotdog is on your plate! (In case you couldn't tell!)

First, create your machine learning model on Machine Learning for Kids:

--- task ---

Open the website [Machine Learning for Kids](https://machinelearningforkids.co.uk/#!/login){:target="_blank"}.

--- /task ---

--- task ---

On the screen that appears, choose **Log in** if your mentor gave you some login details. Enter your username and password on the next screen.

![A picture of the blue log in button.](images/singup_login.png)

Choose **Sign up** if you are creating your own account and follow the prompts to create a new account.

--- /task ---

--- task ---

Select **Go to your projects**.
![Image of the blue 'Go to your projects' button on Machine Learning for Kids.](images/go2projects.png)

--- /task ---

--- task ---

Select **Add a new project**.
![Image of a grey button that reads 'Add a new project'.](images/add_new_project.png)

--- /task ---

--- task ---

Give the project a name and set it to recognise **sounds**.
![](images/name_project.png)

--- /task ---

--- task ---

Select **CREATE**.

![](images/create_button.png)

Once created, click on the project title.

--- /task ---


Now that you have created a project that identifies sounds, you need to set out the different **classes** for your audio — the different words you want the model to classify. In this example, we will use the words `up`, `down`, `left`, and `right`.

--- collapse ---
---
title: Classes and labels
---

**Classes** are the major categories you will sort the audio into. In this case, you need four **classes**: `up`, `down`, `left`, and `right`.

**Labels** are the specific names we give to each audio clip in the training data to help the model identify what is in each clip.

For instance, if you have a clip of someone saying "up" in the training data, you'll label that clip as `up`. By doing this, you're telling the model that this clip belongs to the `up` class. Similarly, if you have a clip of someone saying "down", you'll label it `down`, placing it in the `down` class. Once you train it on this information, the model can be used to predict which class new clips belong to.

![An image explaining that a class is a major category that images can be sorted into. It shows a group of apple pictures in one box, next to an explanation that a label is given to each image to show which class it fits into, with a single apple picture.](images/class_vs_label.png)

You can use as many classes as you want in your model. In this scenario, it's pretty straightforward: every clip is either `up`, `down`, `left`, or `right`. But in other projects, you could have multiple classes based on various characteristics of the data you're working with, such as specific musical instruments, the names of your friends or pets, or songs you like and their genre.

--- /collapse ---

--- task ---

Select **Train**. This will let you add new training data to your model.
![](images/train.png)

--- /task ---

Your model will load and show you a single box on the next page, titled `background noise`. Let's add some samples of background noise now.

--- task ---

If your browser asks you for permission to use your microphone, click **Allow**.

--- /task ---

--- task ---

Click `Add example`. 

![Button that reads '+ add example'.](images/add_example.png)

--- /task ---

In the pop-up box that appears, click the blue microphone to record some 2-second samples of the ambient sound in the room — just whatever is going on around you, but try not to speak into the microphone directly just yet. Remember, you're trying to capture `background noise`!

--- task ---

Record a sample of `background noise` by clicking the microphone. 

![A pop-up box that says "Add example. Record an example of 'background noise'", with a small blue icon showing a microphone.](images/add_background_noise.png)

--- /task ---

--- task ---

When the recording is finished, click the blue **Add** button in the pop-up box:
![A pop-up box that says "Add example. Record an example of 'background noise'", with a small blue icon showing a microphone and a soundprint of the ambient recording.](images/add_bg_noise_2.png)

--- /task ---

--- task ---

Record several samples of the background noise where you are. 

**The minimum required for your model to work is 8 samples**, but remember — the more **training data** you add, the better your model will work!

--- /task ---
