# What is Placeholder?
Here we gonna talk about the placeholder and its uses in our bot

## First why we need placeholder?
We have a big issue without placeholder, which is... dynamic behavior\
Assume You want this behavior:
```
When user send: hi
Bot send: Hi @user
```
Easy right? alright let's try make it\
1- [make a sketch](../tutorials/create.md)\
2- pick [starter](../starters/) as When [user say something](../starters/userText.md)\
3- as for [steps](../steps/) it will be just one step [Send message](../steps/sendmessage)\
4- let's pick the channel to be the starter channel\
5- as for the content.. that's the tricky part
what will be the content?\
as you know we want something.. that changes depends on situation

like if user is `Abdi`\
bot should say: `Hi @Abdi`

if user became `ButterFly`\
bot should say: `Hi @ButterFly`
and so on\
as you see, the content changed and can't be just one message, it can have any possiblitlies depends on which user said it


Here comes Placeholders in the picture

## Placeholder Usages
You now understand why we need it, but how to use it to solve the issue mentioned above?\
it's simple actually, imagine placeholders as a cards that you can use
and these cards given to you by [Starters](../starters/) or [Steps](../steps/)\
For example in [User say something](../starters/userText.md) page
You will find it saying that this starter provides some placeholders
one of them is [`member`](../starters/userText.md#placeholders), and this placeholder contains the user who started the sketch, BINGO! that's what we want 

so in the message content and any [Text](../inputs/text.md) input, you can use placeholder this way:
```
<place holder name>
```
In our example, when [`Send Message`](../steps/sendmessage.md) ask for content we will input:
```
Hi <member mention>
```
![](https://i.imgur.com/dB8iHRi.gif)

Oh wait, isn't the name is `member` what is `mention`?

## Placeholder Properties
Well, you are looking down on placeholder, because it's not as simple\
each placeholder is of specific type like `member` that we used in the previous example is of type [`Member`](../placeholders/member.md)\
and this type provides some useful informations about the user not just `mention` of user\
like let's say you don't want to mention the user actually but just want to print the name of that user
after checking [`Member`](../placeholders/member.md) page, you will find there's exactly a property called `name` that does this so the message will be:
```
Hi <member name>
```
![](https://i.imgur.com/4GXfMnz.gif)

## More Examples
Almost all examples use placeholders\
Click [Here](../examples/) To see examples