# UAL-Coding1-Final

Throughout the semester of Coding One, I have been trying my best to move away from simply modifying the reference code data provided on MIMIC to build a dynamic interactive effect that infuses my own ideas. After becoming familiar with the way javaScript code is written and the way images are rendered by the teacher, I think I can do my best to complete this little interactive comic at this stage.


The theme of the comic is that just before Christmas, just like now, Santa and his moose see a depressed DJ who, according to their Christmas workshop profile, has been depressed for a long time. Santa decided to give this person who had worked so hard for her dream a little Christmas present - she could see the snowflakes outside her window change to the music when she used the DJ console.
I seperated the idea down into the following parts: the storytelling images of the comic body and the pagination control, the generation and animation of the snowflakes, the DJ console operation and the changing of the 3D graphics on the disc, and how the dj music itself is generated and called up in the Maximilian Library.


The images and audio were generated in the same way as the teacher provided reference calls and modifications this term, and I will talk more about how I made these ideas come together in practice and the new things I learnt from working on this project.
Considering that the entire code for this project required importing a large number of images and audio files, I had realised during week7 that MIMIC had limited image space and wrote all my code in VS Code in order to prevent the images from not loading due to excessive memory. In order to load the images better, I found that the http-server in terminal was a good solution to this problem, as it helped me to upload the images to the network first.


After setting up the canvas and using the draw() and draw2() functions to differentiate the number of pages in the comic, I set up snow() and Rundisc() to control the snowflake generation and the change of the 3D effect on the disc called in draw2() respectively. snow() and Rundisc() have a number of variables of their own which change with each frame loaded. I once added a random variable of x to snow() where the image was generated each frame, I intended to change the value of x the next time the snowflake was generated, but this resulted in the snowflake flying around in the image. This problem was solved before I moved the random variable for x to the topmost global variable section to generate the snowflake.
The use of loops and putting the image parameters into the Array as an Object allowed me to better control the appearance of the image.


After breaking out of MIMIC I got a warning that the audio section would not play, and after checking the documentation and asking around with fellow coders I found out that this was a browser protection measure to prevent the user from automatically opening certain audio and video when viewing a web page. So when I needed to play a sound effect in the second act, I added a section that played music when clicked, and the problem was solved.

There is still a lot of room for improvement, but I am happy that I have finished this work. Every programming session is an exploration: for example, I was curious if there were layers in the canvas and this time I practiced and understood that the top-down running of the code is how the layers are rendered from the bottom to the top. To be honest, I think Coding One is full of knowledge and it really made me feel anxious on the path of learning to explore programming. But the results of the code I wrote with the help of my classmates and teachers made me feel happy, and in that mood this work was born.
