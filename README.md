# Deep Learning Lab1 Report
  The lab is about using ESPnet toolkit to train Hakka speech data and translate it into text.
The following content shows how to build and complete the task.

##1. training data:
  The training data we use is from [Kaggle completion website](https://www.kaggle.com/competitions/espnet-taiwanese-asr1/data), provide by TA, which is a bunch for Hakka voice data and training text, notice that the text we use are the pronounciation that ignoring tones to reduce the complexity of training.
  The training data is placed at thge following location in ESPnet, using Aishell training model as example:

>espnet/egs2/aishell/asr1/downloads
>>data_aishell
>>>transcript
>>>>aishell_transcript.txt (_transcript file,template of transcripting voice into text_)

>>>wav
>>>>dev (_put random example voice data file_)
>>>>test (_testing data voice file_)
>>>>train (_training data voice file_)
>>resource_aishell
>>>iexicon.txt (_lexicon file_)
>>>speaker.info (_one global speaker only_)

##2. training:
  The step of training are almost same as the [ESPnet example](https://github.com/espnet/espnet) but using aishell as model, and the code file also has the description about every part of the code. Noticed that we need to adjust some setting by ourselves including prevent automatically downloading data(since we already have our training data), adjusting batch size, epoch and GPU, etc. The code file has further information about how and why we need to adjust.
  
##3. model:
  The model I use is aishell in espnet/egs2. it is a transformer model. Unfortunately, I'm just a layman and don't know much about the field, so I can't and nor do I dare to explain this, lets hope the respectful professor can talk about more of this in the later course.
  
##4. result:
   My error rate is about 10%, which is awful comparing to other students joining the completion, Sadly, I just following what TA teaches and didn't change the training process a lot, I tried to figure out by myself or others, but my friends said that they just also followed the steps TA gave, too. So in the end, I can only guess the reason is probably because of hardware computation ability.
   
##5. Comment:
  I'll say that I can't help but feeling a little bit furstrated about this lab, I tried many times and even pay for CoLab pro. but in the end the result isn't that good for me. The batch size and training epoch I can set is pathetically low since it is limited by GPU and its RAM. There is a feeling that the lab is a pay-to-win project. But to be honest, it's my responsibility to optimize the model and not just complain about the lab. So I'll do my best trying to learning DL knowledge, and hoping that table will turn when doing next lab.
