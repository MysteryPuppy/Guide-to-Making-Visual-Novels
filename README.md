# Guide to Making Visual Novels
### How anyone can turn a story into a game with no programming experience
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/home.png "Example visual novel")
If you ever wanted to be able to tell a story visually but didn't quite know where to start or felt intimidated by the coding aspect of making a visual novel, this guide is for you. I just spent the summer teaching children ages 10-18 how to code their own visual novels and I can hereby say that I know that *anyone* can create an amazing game. With a little bit of time, and after understanding of some basic concepts, creating a visual novel these days is very intuitive and a fun process.

Again, **no** prior coding experience is needed. Let's get started!

#### Getting Started & The Basics

1. To code our visual novel, we're going to be using a game engine called [Ren'Py](https://www.renpy.org). If you visit their site, it's quite easy to install the engine on your Windows, Linux, and Mac machine. Ren'Py allows the user to code in a simple script language derived from Python.

2. Once Ren'Py is downloaded, open the application and I'll tell you a little bit about how everything is set up. This is how Ren'Py should look when you open it (it might look slightly different depending on what OS you're using. I'm on Mac.):
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/1.png "Ren'Py on startup")
On the left you have two default projects: *Tutorial* and *The Question.* The Question is a visual novel which showcases what Ren'Py can do and I recommend giving it a quick play-through (you can play the game by pressing "Launch Project" in the bottom right) so you understand what we'll be working towards. Tutorial actually shows how to use Ren'Py and it's a good place to start if you want to. I'll walk you through everything you need to know to get started though in this guide.

3. To get this guide on the road, we're first going to create a new project. To do this, click on "+ Create New Project" on the bottom left. It will come up with a window that says "INFORMATION" on it and you can just click "Continue." Next, enter a name. I'm going to be putting in the name "FHTY" since I'm using all the assets in this tutorial from a game I created recently that is called [From Here to You](https://github.com/lovebirdsnest/From-Here-to-You). Feel free to download and use assets from this project for your example game if you want. Press continue, choose your game size (I'm using 1280x720), press continue, and choose the colors you want your game to have. These colors don't mean too much since you can change the entire GUI later if you want. That's a *bit* more advanced though. Perhaps in a second tutorial I can go over Ren'Pys more advanced features. For this tutorial, just pick some colors you think look nice. After you pick the colors, your game will be created and will appear under the "PROJECTS" heading.

4. If you select your project on the left side, you'll see that on the right side of Ren'Py you have some interesting headings like "Open Directory", "Edit File", and "Actions." The options under "Open Directory" will open the folder where those assets are saved on your computer. For instance, if you click "images" it will open where the images for your game are saved on your computer. This is useful when we want to quickly see which images our game is using and add/modify them. Another important option is "game" which will open up where the main script files are. The options under "Edit File" show important files that contain the code for our game. The most important of these is `script.rpy` where all of our character dialogue, background changing, etc. is. The "Actions" options aren't usually used until you have completed your game and wish to export it into an application.

5. So, let's get started with the coding why don't we. Click on `script.rpy` from under the "Edit File" heading and it will ask you which text editor you'd like to use. Choose your favorite. I personally like to use [Atom](https://atom.io) but the choice is yours. You can also just drag the `script.rpy` file (from where it is on your computer) into your text editor and it will open that way as well. Once the file is open it will look like this:
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/2.png "script.rpy")
There's not a lot of code in this file yet but Ren'Py does put in some default code to get things going. I'll explain some of the basics with what they've already entered here.
**Remember: the best way to learn how to do something is to do it so it's good to follow along.** We see that at the top of file there is `define e = Character("Eileen")` which defines a new character whose name is "Eileen" and whose alias is `e`. Now, when you see the use of `e` on lines 27 and 29, you know that it's "Eileen" speaking these lines. <mark>All dialogue in Ren'Py is surrounded by quotation marks. When a character is speaking, there is a letter (or word) like `e` in front of the words in quotations. If the words in quotations are not meant to be spoken by anyone, there is no letter or word in front of it.</mark> For example, I'm going to add these two lines above the rest of the quotes.<br/>`"This is our first Ren'Py game."`<br/>`e "This is going to be so fun!"`<br/>
How my code looks:
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/3.png "Added lines to script.rpy")

6. Now we're going to see what this changed in our game. To test what we have so far, go back to the Ren'Py application and on the bottom right, press "Launch Project." Once you've launched the project and have pressed "start" you'll see the dialogue we entered into our code. You'll also see that the name "Eileen" appears over the dialogue that had the `e` in front of it. Congratulations! You know know how to create dialogue 🎉 The only problem is...It doesn't look so good with no images put in yet. Don't worry, there is a simple fix to this! <br/>
I'm going to be using the assets I used in my game. But I'll also teach you how to make your own since ultimately you're going to need to know how to do that. For <mark>character images, I use the dimensions 456x700</mark> and for <mark>background images I use 1280x720</mark>. Of course, if you chose a different game dimension size you'll want to change your background dimensions to that. Also you don't have to make your character this size. It's just a size I've found to be good when making my games in the past. <br/>
To make your character, just open your image editor (I reccomend Photoshop or Paint Tool Sai) and make a canvas 1280x720 pixels large. Next, make sure your bottom layer is transparent, and create a new layer on top of it. Draw how you want your character to look and then once you're done, export it as a PNG into the "images" folder of your game (which, again, you can pull up by clicking the "images" option under "Open Directory").
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/4.png "Character in Photoshop with transparent background")
You can also create a background in the same way, with just a different canvas size. The background also shouldn't be transparent, so fill that sucker in. Export the background as a PNG as well and save in the "images" folder.<br/>
<mark>A note on Ren'py naming conventions:</mark> backgrounds should be saved as `bg [name].png` for example: `bg bedroom.png` and characters should be saved as `[name][action].png` for example: `eileen happy.png`. By the end of your game, you'll probably have many images saved here.
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/5.png "Lots of images saved")

7. Now that we have our images prepared (you don't have to have all of them done yet, of course) we can start making our game look like the real deal. To do this, switch back to your text editor and we're going to create a new character. Now, I'm going to create a new character named "Kiwi." Do you remember how to create new characters? We can create a new character by writing `define k = Character("Kiwi")`. Okay, now we have defined "Kiwi" and I'm going to simply delete the default text that Ren'Py put into our file other than the `label start` and `return` at the end. I'm going to also make our character say something by writing `k "Good morning!"`
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/6.png "How our code looks")
Now comes the part where we put our images to life. To show a character image on the screen, you simply write `show [name][action]` or, in this case, `show kiwi normal` since I saved my file as `kiwi normal.png`. I'm going to put this right before kiwi says his line. You can also tell Ren'Py where to put the character on the screen by writing `show [name][action] at [right/left]`. In this case I want Kiwi on the left of my screen so I'll write `show kiwi normal at left`. <br/>
This is good, but we're still missing the background. To add a background, all you have to do is type `scene bg [name]`. Here, I'm going to use my bedroom scene and type `scene bg bedroom` above `show kiwi normal at left`.
What our code looks like so far:
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/6.png "How our code looks")
And how it looks when you launch the game:
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/8.png "How our game looks")

8. It's starting to look like a real game, right? Well, not quite but it's getting there! Let's add and polish some things up. To add a second character, I'm going to define a new character under kiwi's definition named Melon. To do this I'll write `define m = Character("Melon")`. We can show Melon in the scene the same we showed Kiwi. Under where we wrote `show kiwi normal at left`, let's write `show melon normal at right` so that the two characters don't overlap each other. Now we have two characters on the screen and can have them talk to each other. Remember, to <mark> hide a character, just write `hide [name]`.</mark> Another thing we can do is give them each different colors for their names. To do this, when we define the characters, we just have to write it like this: `define k = Character(_("Kiwi"), color="#C3FFC6")` where `#C3FFC6` is the color hex code I want Kiwi's name to be. You can find color hex codes [here](http://www.color-hex.com).<br/>
To change a character's emotions, you don't have to hide the character. Just write `show [character][new action]` again and it will change the character's image.
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/10.png "How our code looks")
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/11.png "How our game looks")
**Test yourself:** Try to change your characters' expressions and the backgrounds! Then make both of your characters have a conversation with each other. Add more dialogue to your code to start creating a cohesive story.


#### Using Menus
1. Okay, the basics are taken care of but now you're probably wondering how we can allow the user to make choices. Without them being able to make choices, it's not much of a game, is it? To allow the user to make a choice, we have to create a `menu`. To create a menu, all you have to write is:

```
menu:
        m "Oh my weekend..."

        "It's been great!":
            jump great
        "It could be better":
            jump notgreat

```
2. The first line `m "Oh my weekend..."` appears in the dialogue box under the options and `"It's been great"` and `"It could be better"` are both the choices that the user can click on. The colon after the two choices is **important** so don't forget it. Then on the lines `jump [label]` underneath them, remember to tab them in since this is python-based and after colons in python you tab in the next line. When you `jump [label]` it tells Ren'Py to look for the label name lower in the code. This means that we have to create some new labels!<br/>
Labels are pretty simple to make and we actually already have a label in our game already. The code `label start` near the beginning of our code is a label called "start". We're going to be making two new labels "great" and "not great." Once you make the labels, you can continue how you want your story to go. **Note:** There can be more than 2 options in a menu, just continue to add options in the same way we showed above.
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/12.png "How our code looks")  
3. Test this code out and you might run into an issue however. If you click the option "It's been great" we get both responses. This is because label great doesn't have a `return` or a new `jump` so it just goes down to the next label automatically. To remedy this, you can just make it jump to a new label (maybe one both of our created labels can jump to, to rejoin them again) or just put a `return` statement in there to end the game. I'm going to be merging my labels again and then ending the game so that you can see how one goes about using labels a little more.
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/13.png "How our code looks")

#### Changing the Main Menu Picture
1. to make our game look nice to new players, let's change the main menu picture so we're not just staring at a solid color. To do this, open "gui" under "Open directory" on the Ren'py application.
2. Once this opens, look for a file called `main_menu.png` and open it in your image editor. Color/replace the solid color with whatever you want your game menu image to be. Once you're done, save your image and it should appear on the screen the next time you launch the game.  
3. When you launch the game, you'll notice that the name of the game still appears in the bottom right hand corner. If you don't want the name of your game to appear there, don't fret. Open the `options.rpy` file from under `Edit File` and find the line that says `define gui.show_name = True`. Change `True` to `False` and you're good to go.
![alt text](https://github.com/lovebirdsnest/Guide-to-Making-Visual-Novels/blob/master/images/9.png "How our game looks")  

Alright, that just about wraps up this guide! A second guide on how to use Variables, create GUI modifications, and more to be in an upcoming tutorial~! I hope you learned something about creating visual novels and until next time, keeping creating & having fun 🎮
