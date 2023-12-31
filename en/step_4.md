
## Make a Scratch application to classify sounds

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Your model is trained, tested, and ready to use, but to do that you need to create a Scratch project that allows your user to speak into the microphone and then classifies the input as `up`, `down`, `left`, or `right`.
</div>
<div>
![Image showing the Scratch cartoon cat saying 'I hear Up'.](images/demo_shot.png){:width="300px"}
</div>
</div>


### **Your project will:**
+ Take audio input from the user
+ Use your trained ML model to classify sounds
+ Move a sprite the on screen based on the classification

--- task ---

On your [**project page**](https://machinelearningforkids.co.uk/#!/projects){:target="_blank"}, select **Make**:
![Image showing a button reading 'Make' and the explanation 'Use the machine learning model you've trained to make a game or app, in Scratch, Python, or App Inventor'.](images/make_button.png)

--- /task ---

--- task ---

On the next page, select **Scratch 3**
![](images/scratch3_button.png)

--- /task ---

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
A special fork of Scratch will open in a new tab. When it does, you will see an item in the left-hand menu with the same name as your machine learning project.

The new grey blocks you can see in that menu allow you to access your machine learning model from within your project:
</div>
<div>
![Image showing several Scratch block menus, with the final one being titled MusicWellness with the Machine Learning for Kids logo.](images/model_blocks_menu.png){:width="100px"}
</div>
</div>

--- collapse ---
---
title: Pro tip - Save your work!
---

This special version of Scratch allows you to access your machine learning model, **but** if you try to open your project in another version of Scratch online **it won’t work**. 

A solution to this is to save your work to your computer. Once you have the .sb3 file for your project saved, you can open it again later, or on another computer:
+ Go to [rpf.io/mlscratch](rpf.io/mlscratch){:target="_blank"} to get to this special fork of Scratch 
+ Once Scratch opens choose **File** > **Load from your computer**
+ Select your file in the window that appears to return to where you left off

![Image showing the Scratch file menu with the 'Load from your computer' option highlighted.](images/load_menu.png)


Save your work as often as you can to make sure you don’t lose any progress!

--- /collapse ---

--- task ---

From the yellow `Events`{:class="block3events"} block menu, add a `when green flag clicked`{:class="block3events"} block to your workspace. This is the script that will run the first time you start the project. 

```blocks3
when green flag clicked
```

--- /task ---

--- task ---

From the blue `Motion`{:class="block3motion"} menu, add a `set rotation style [left-right]`{:class="block3motion"} block to your script.

```blocks3
when green flag clicked
set rotation style [left-right v]
```

This will make sure your sprite doesn't flip upside-down when moving around.

--- /task ---

--- task ---

Next, drag a grey `train new machine learning model` block from the Machine Learning for Kids menu at the very bottom:

```blocks3
when green flag clicked
set rotation style [left-right v]
train new machine learning model :: #4b4c60
```

--- /task ---

--- task ---

Next, from the golden `Control`{:class="block3control"} menu, add a `wait until < >`{:class="block3control"} block to your script.

```blocks3
when green flag clicked
set rotation style [left-right v]
train new machine learning model :: #4b4c60
wait until <>
```

--- /task ---

--- task ---

Into the empty slot in the `wait until < >`{:class="block3control"} block, drag a round `is the machine learning model [ready to use] ?` block from the Machine Learning for Kids menu at the very bottom:

```blocks3
when green flag clicked
set rotation style [left-right v]
train new machine learning model :: #4b4c60
wait until <is the machine learning model [ready to use v] ? :: #4b4c60>
```

--- /task ---

--- task ---

To the end of this script, add a grey `start listening` block from the Machine Learning for Kids menu at the very bottom:

```blocks3
when green flag clicked
set rotation style [left-right v]
train new machine learning model :: #4b4c60
wait until <is the machine learning model [ready to use v] ? :: #4b4c60>
start listening :: #4b4c60
```

--- /task ---

Your application is now ready to start listening once you click the green flag. Next, you need to add some instructions for the sprite to follow when the model classifies each word.

--- task ---

From the Machine Learning for Kids menu, drag in several blocks — one for each word your model is trained on:


```blocks3
when I hear left :: #4b4c60 hat
```

```blocks3
when I hear right :: #4b4c60 hat
```

```blocks3
when I hear up :: #4b4c60 hat
```

```blocks3
when I hear down :: #4b4c60 hat
```

--- /task ---

--- task ---

From the blue `Motion`{:class="block3motion"} menu, add a `change x by (10)`{:class="block3motion"} to the `when I hear left` and `when I hear right` blocks:


```blocks3
when I hear left :: #4b4c60 hat
change x by (10)
```

```blocks3
when I hear right :: #4b4c60 hat
change x by (10)
```

--- /task ---

--- task ---

Beneath the `when I hear left` block, change the value in the `change x by (10)`{:class="block3motion"} block to say **-10**:

```blocks3
when I hear left :: #4b4c60 hat
change x by (-10)
```

```blocks3
when I hear right :: #4b4c60 hat
change x by (10)
```

--- /task ---

Your sprite can now move from side to side when you say "left" or "right". Now add some controls for up and down!

--- task ---

From the blue `Motion`{:class="block3motion"} menu, add a `change y by (10)`{:class="block3motion"} to the `when I hear up` and `when I hear down` blocks:


```blocks3
when I hear up :: #4b4c60 hat
change y by (10)
```

```blocks3
when I hear down :: #4b4c60 hat
change y by (10)
```

--- /task ---

--- task ---

Beneath the `when I hear down` block, change the value in the `change y by (10)`{:class="block3motion"} block to say **-10**:

```blocks3
when I hear up :: #4b4c60 hat
change y by (10)
```

```blocks3
when I hear down :: #4b4c60 hat
change y by (-10)
```

--- /task ---

--- task ---

**Click the green flag.** Wait for the model's status to be 'listening', and say the words "left", "right", "up", and "down".
You should see you sprite begin to move!

--- /task ---

You have now trained your own machine learning model to classify speech, and used that to control a character in Scratch! 

In the next step, you can customise the way your application looks by adding costumes and some new features that activate depending on the classification of your input.

