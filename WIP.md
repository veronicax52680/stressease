# StressEase

## Current and Future Prospects (in no particular order)
This is more of a resource for me to keep track of what I want to improve for StressEase 2.0, but you are welcome to take a look at my future endeavors! 

### Real-Time Data Analysis For Immediate Feedback
Currently, StressEase requires manually running Python files and analyzing data that has already been collected. This is less than ideal because we can't get immediate feedback and act on our stress responses right away, rendering this project useless for day-to-day use. My next step is to update the pipeline where CSV data is collected and analyzed at the same time.  

### Improve Accuracy
I will deep-dive into the algorithms that go into calculating the BPM and skin conductance, and I will customize them to make it more accurate. I will also integrate some new sensors into StressEase, such as a motion and temperature sensor, to collect data that is more accurate. Camera and computer vision might come in handy as well, though I would need to research safety and privacy concerns. 

The project currently depends on classification, which is simply a "yes" or "no". There is no nuance that determines if you are "super stressed" (5) versus "a little bit stressed" (1). I will experiment with different ML algorithms and most likely move to regression instead of classification. 

Finally, I will experiment with designing my own sensors for even more accuracy.

### Interface Changes
StressEase currently runs on the terminal. This cuts out inexperienced tech users who may benefit from this biomedical device. I will experiment with creating a GUI in two ways. First, I will display graph results on an LCD screen connected directly with the device. Second, I will create a mobile app so data can easily be accessed on phones. I am also thinking about creating a website to store long-term data, though I will need to research the ethics and security of data storage. 

I will also think of ways to wear this device. I could design a watch, necklace, or other types of wearables through 3D modeling and 3D printing. 