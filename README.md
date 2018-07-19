# cloth-recognition-version2
This is my 2nd attempt on this topic.

### My thoughts on this.
While research on this topic, I chanced upon this [Kaggle competition](https://www.kaggle.com/c/imaterialist-challenge-fashion-2018). In their discussion, the winner and 3rd place winner just simply used all the pre-train model and retrain it without freezing and still get pretty good result (Leadership board 0.72483 max). I want to know whether it is "even possible" to achieve better result JUST by using an advance model (Faster_RCNN) without the use of attributes. If this works well, then the problem to by previous attempts is just fine-tuning my custom CNN parameters, and I had to take ROI into consideration. 

Previously if you recalled, there is another technique to use Google's tensorflow Object detection code but I have trouble. Since this is the only method (I know) that uses XML annotation and I can train images on a Faster_RCNN model. I decided to relooked into it and result is quite a success.
OK, OK.. I know.. this is not my codes. Maybe next time when I am more skilled I will code faster-rcnn from scratch. 
