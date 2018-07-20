# cloth-recognition-version2
This is my 2nd attempt on this topic.

### Here's what I think:
While research on this topic, I chanced upon this [Kaggle competition](https://www.kaggle.com/c/imaterialist-challenge-fashion-2018). In their discussion, the winner and 3rd place winner just simply used all the pre-train model and retrain it without freezing and still get pretty good result (Leadership board max 0.72483). 
[Previously if you recalled](https://github.com/noelcodes/Clothes-recognition), there is another technique which I know, called [tensorflow model API](https://github.com/tensorflow/models) but I hit into some error while working on xml_to_csv, I then gave up. This time, I re-look on this again. Followed a [Youtube tutorial](https://www.youtube.com/watch?v=Rgpfk6eYxJA), I was able to train fashion dataset on Faster_RCNN model with XML annotation's XY information. I want to know whether it is possible to achieve better result JUST by using a more advance model (Faster_RCNN) without the use of attributes. If this works well, then the problem with by previous attempts is just fine-tuning my custom CNN parameters, and I had to take ROI into consideration. 

### Result:
Trained for almost 5 hours, after 96523 epochs, see tensorboard below, the lost managed to goes as low as 0.03841, not too bad. Not sure how to use tensoreboard to show accuarcy, sorry.

![alt text](https://i.imgur.com/gYBLyva.jpg)

See [Juypter: Test On 100 static images](https://github.com/noelcodes/cloth-recognition-version2/blob/master/noel_static_picture_demo.ipynb) : Let's loop this model over test images. Wow... it performed pretty good.


Let's try this on google images real time. I did a video demo. It's pretty OK. At least now it managed to identify many clothes correctly. Click below to enlarge video.

[![LIVE DEMO](https://github.com/noelcodes/cloth-recognition-version2/blob/master/ezgif.com-video-to-gif%20(3).gif)](https://youtu.be/bHOmGZ0q58o)

Conclusion: Why I choose Faster_RCNN? Because I found this table below in one of the papers. Well Faster_RCNN model works pretty well as you can see. I think the XML's ROI information helps a lot as well. 

![alt text](https://i.imgur.com/AK9BXTu.jpg)

### Next step:
OK, OK.. I know.. the above is job well done by Google. Reminder, my knowledge on computer vision is only 2.5 months ago. It's has always been my wish to code faster-rcnn from scratch, maybe start from using keras, which I'm more familiar. I found this githb repo for reference. Let's do this, and try this without API...

Work in progress......



