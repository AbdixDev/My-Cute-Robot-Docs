# Hugger
Let's see how our cute robot can be used to hug people
## Goal
When the user send `hug @user`\
Our bot should send a random hug GIF like\
![https://i.imgur.com/T0XXQIl.jpg]
## Steps
1- Send `-create` in the server, and name the sketch `Cute Hugger` (it can be anything)\
![](https://i.imgur.com/k1gRirY.jpg)

2- Which Starter will we use?\
It will be [`User Say Something`](../starters/userText.md) starter \
![](https://i.imgur.com/N6iobsJ.jpg)

3- It will ask us to start when user send what text? Let's send `hug`\
![](https://i.imgur.com/1FFGHsX.jpg)

4- It will ask for which matching type?\
in this situation, we want this starter to start when a message starts with `hug`. so let's select `Starts with`\
![](https://i.imgur.com/jL1h7J1.jpg)

5- Now, case sensitivity? let's make him case insensitive, so it accept `Hug, HUG, hUg` as well
![](https://i.imgur.com/M75xNul.jpg)

6- Okay starter is done, time to add the sketch's [steps](../steps/)\
1st step will be [send message](../message/sendmessage.md)
![](https://i.imgur.com/XeSVPRh.jpg)\
![](https://i.imgur.com/WOU75da.jpg)

7- Which channel? well, bot random gif should be sent in the same channel as the starter\
![](https://i.imgur.com/CjhZvIN.jpg)

8- What is the message content? we will use the [placeholder](../tutorials/placeholder.md) to get the user mention, and whatever he mentioned inside the message through the [starter placeholders](../starters/userText.md): [`message`](../placeholders/message.md), [`member`](../placeholders/member.md)\
Let's send: 
```
<member> hugs <message mentions>
https://c.tenor.com/NGFif4dxa-EAAAAi/hug-hugs.gif
```
9- Save!
![](https://i.imgur.com/nHZ2imW.jpg)

10- Let's test it out by sending `hug @user`\
i will just hug me 😢
![](https://i.imgur.com/x7wdcvJ.jpg)

11- It worked! but... that's not random, it will always send same gif, next part we will just add an extra step to give random gif, we will re-do the previous steps from 1 to 5 but instead of adding `send message` as step 1 we will select [`random text`](../steps/randomtext.md)
![](https://i.imgur.com/E33TX0w.jpg)\
![](https://i.imgur.com/0CsF31u.jpg)

12- Random Input, requires us to input each text separated by `;`+`new line (enter)`\
Let's enter the gif links
![](https://i.imgur.com/TzbiDxK.jpg)

13- Then add next step to be [`send message`](../steps/sendmessage.md), channel as `starter channel` but on content it will appear a menu\
we will select `custom`\
![](https://i.imgur.com/WRY3tCT.jpg)

14- then it will ask for custom content, let's send:
```
<member> hugs <message mentions>
<randomtext1>
```
> Take note of <randomtext1> this [placeholder](../tutorials/placeholder.md) is provided by the [random text step](../steps/randomtext.md) we added in step 11

![](https://i.imgur.com/SZ1hSaI.jpg)

15- That's it :tada: , Save the sketch!

## Result
Try send `hug @user` twice or more\
![](https://i.imgur.com/T0XXQIl.jpg)
