# Google-colab-experiments
Experiments with cloud computing

Cloud Computing 2021 - Learning Diary
Noora Angelva
 
Exercise 1 - Google Experiments, Teachable Machine

Using the Teachable Machine was easy, but quickly realized how many images the machine needed and the different versions of it to identify correctly. I created three classes of pen, glove and phone. When I tried a black pen that was on a guy’s Teachable Machine I thought it was a phone exactly the same in what position the pen was placed. The pen taught was red and the phone I taught Teachable Machine to learn to recognize the phone was black. I guess that for this reason came error detection. Also, in a situation where my face alone was in front of the camera, it was identified by the phone. I guess this is because my face was only visible in the tutorials on the phone.
By copying the luo keras_model.h5 file to Drive, (The template can be downloaded via the "Export Model" button. Select Tensorflow -> Keras -> Download my model), I got it easily available in Google colab so I could experiment with my own image to see if the Teachable machine recognizes the image. properly. The codes and test files are in their own folder “Cloud1Image”.
from keras.models import load_model
from PIL import Image, ImageOps
import numpy as np
from google.colab import drive
drive.mount ('/ content / drive')
Load the model
model = load_model ('/ content / drive / MyDrive / Pilvilaskenta2021_Noora_Angelva / keras_model.h5')

I also tried voice recognition on Teachable Machine, but I didn’t transfer it to Google Collab. I noticed that a lot of sound clips are needed for voice recognition. Once I had taught it to recognize the two classes it was very uncertain to determine the sound of the second of the options alone, although the sound of the second class was not heard at all when testing how well the recognizer had learned.
I feel that Teachable Machine is well suited for learning machine learning, but I don't find it to be a sensible solution for real / bigger projects. Its accuracy is not very good and it would need a huge amount of data to be accurate enough and to be able to filter out extra background noise from affecting recognition. I’m not sure, but I bet Teachable Machine can’t handle that much data, but rather created for reference.

Exercise 2 - Google Collab, Style transfer

Style transfer is an optimization technique that can be used to take two images, a content image and a style reference image (such as a work of art by a famous painter). The end result is a content image "painted" in a style image style. That is, take a basic income image, a content image that you want to reconcile, and a style image that you want to reconcile. Edit the base image by minimizing content and style distance (loss) by retrieval and creating an image that matches the content of the content image and the style of the style image.
I first tried to make the images through a shorter formula. I uploaded the images via colabiin driven. The end results of the shorter version were on top of the spotted look. The end result was not so much inspired by a style image / work of art, but one big thing was taken from the image and reproduced within the different boundaries of the underlying image in the colors of the style image.


I didn’t think the end result was very eye-catching.

When done through a longer formula, the result was very different. Its only downside was that it took significantly more time than the shorter one, i.e. not so accurate when done, which took a couple of seconds. In a more detailed Style transfer, there are 10,000 steps for deep learing, which takes a lot of time and computing power myself, I have often used 100 steps.


The more advanced version still doesn't always succeed in what was sought ...
If this were in an application or otherwise widely utilized, I would bet that very few would be able to wait for a job to be completed if it took five seconds longer, not to mention a few hours. Of course, the imprint is much better. The use of artificial intelligence requires continuous optimization and finding a middle ground between time and quality. In Google Collab, the more accurate Style transfer finally created a new version of the image in five minutes when the Hardware Accelerator was put on as a GPU.
This could and certainly is already used in many applications. The first thing that comes to mind is the editing of the image when posting to Some and in advertising descriptions, for example. This would make it easy to “create” art for your home based on your own images and customize their style to look “more expensive”. In games and VR games, Style Transfer could also be used or may already be used. This way, games could be customized to look what the player wants, just as characters are already customized in games.

Exercise 3 - Google Collab, DeOldify

I didn’t add to this connection about myself, I prefer to use pictures of my dog. Deoldify seemed to produce the best results from the sky and water, but a rare lousy coloring attempt was a sup-board coloring that the algorithm left completely uncolored. I would assume that the neural network still has something to learn here.


 The first picture
