# cloth-recognition-version2
This is my 2nd attempt on this topic.

### Here's what I think:
While research on this topic, I chanced upon this [Kaggle competition](https://www.kaggle.com/c/imaterialist-challenge-fashion-2018). In their discussion, the winner and 3rd place winner just simply used all the pre-train model and retrain it without freezing and still get pretty good result (Leadership board max 0.72483). 
Previously if you recalled, there is another technique which I know is to use [tensorflow model API](https://github.com/tensorflow/models) but I hit into some error then gave up. I re-look on this again. Followed a [Youtube tutorial](https://www.youtube.com/watch?v=Rgpfk6eYxJA), I was able to train fashion dataset on Faster_RCNN model with XML annotation information. I want to know whether it is "even possible" to achieve better result JUST by using a more advance model (Faster_RCNN) without the use of attributes. If this works well, then the problem with by previous attempts is just fine-tuning my custom CNN parameters, and I had to take ROI into consideration. 

### Result:
Trained for almost 5 hours, after 96523 epoch, see tensorboard below, the lost managed to goes as low as 0.03841, not too bad. Not sure how to use tensoreboard to show accuarcy, sorry.

![alt text](https://i.imgur.com/gYBLyva.jpg)

Let's loop this model over test images. Wow... it performed pretty good.
See [Juypter: Test On 100 static images](https://github.com/noelcodes/cloth-recognition-version2/blob/master/noel_static_picture_demo.ipynb)

Let's try this on google images real time. I did a video demo. It's pretty OK. At least now it managed to identify many clothes correctly. Click below to enlarge video.
[![LIVE DEMO](https://github.com/noelcodes/cloth-recognition-version2/blob/master/ezgif.com-video-to-gif%20(3).gif)](https://youtu.be/bHOmGZ0q58o)


### Next step:
OK, OK.. I know.. the above is job well done by Google. Just a reminder, my knowledge on computer vision is only 2.5 months ago. It's has always been my wish to code faster-rcnn from scratch, maybe start from using keras, which I'm more familiar. I found this githb repo for reference. Let's do this...

Work in progress......



