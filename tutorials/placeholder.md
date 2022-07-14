# What is Placeholder?
Here we gonna talk about the placeholder and its uses in our bot

## First, why do we need a placeholder?
We have a big issue without placeholder, which is... dynamic behavior

Assume You want this behavior:
```
When User send: hi
Bot send: Hi @user
```
Easy right? Alright let's try to make it\
1- [make a sketch](../tutorials/create.md)\
2- pick [starter](../starters/) as when [user say something](../starters/userText.md)\
3- as for [steps](../steps/) it will be just one step [Send message](../steps/sendmessage)\
4- let's pick the channel to be the starter channel\
5- as for the content.. that's the tricky part.
What will the content be?

As you know, we want something that changes depending on the situation

Like if the user is `Abdi`\
Bot should say: `Hi @Abdi`

If user became `ButterFly`\
Bot should say: `Hi @ButterFly`
and so on\
As you can see, the content changed from Abdi to ButterFly by using the placeholder - member - the possibilities are endless. It changed depending on the User. The response did not stay the same.

Here comes Placeholders in the picture

## Placeholder Usages
You now understand why we need it. To explain further...
It's simple actually. Imagine placeholders as cards that you can use
and these cards are given to you by [Starters](../starters/) or [Steps](../steps/)\
For example, in [User say something](../starters/userText.md) page, you will find it saying that this Starter provides some placeholders,
one of them is [`member`](../starters/userText.md#placeholders), and this placeholder contains the User who started the Sketch. BINGO! That's what we want 

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
