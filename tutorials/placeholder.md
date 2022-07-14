# What is Placeholder?
Here we gonna talk about the placeholder and its uses in our bot

## First, why do we need a placeholder?
We have a big issue without placeholder, which is... dynamic behavior

Assume you want this behavior:
```
When User send: hi
Bot send: Hi @user
```
Easy, right? Alright. Let's try to make it:\
1- [make a sketch](../tutorials/create.md)\
2- pick [Starter](../starters/) as when [User Say Something](../starters/userText.md)\
3- as for [Steps](../steps/), it will be only one step -> [Send message](../steps/sendmessage)\
4- let's pick a channel that will be the starter channel\
5- as for the content.. that's the tricky part.
What will the content be?

As you know, we want something that changes depending on the situation

Like if the user is `Abdi`\
Bot should say: `Hi @Abdi`

If user became `ButterFly`\
Bot should say: `Hi @ButterFly`
and so on\

As you can see, the content changed from Abdi to ButterFly by using the placeholder - member. It changed depending on the User. The response did not stay the same.

Here comes Placeholders in the picture

## Placeholder Usages
You now understand why we need it.
To explain further...
It's simple actually. Imagine placeholders as cards that you can use
and these cards are given to you by [Starters](../starters/) or [Steps](../steps/)\
For example, in [User Say Something](../starters/userText.md) page, you will find it saying that this Starter provides some placeholders,
one of them is [`member`](../starters/userText.md#placeholders), and this placeholder refers to the User who triggered the start of the Sketch. BINGO! That's the one we want. Instead of a simple and standard response from the bot, the placeholder called member can actually specifically respond to the User! With placeholders, the possibilities are endless! You can make the bot do much more.

So in the message content and any [Text](../inputs/text.md) input, you can use placeholder this way:
```
<place holder name>
```
In our example, when [`Send Message`](../steps/sendmessage.md) asks for the content, we will input:
```
Hi <member mention>
```
![](https://i.imgur.com/dB8iHRi.gif)

Oh wait, isn't the name `member`? What is `mention`?

## Placeholder Properties
Well, you are looking down on placeholder, because it's not as simple as that.\
Each placeholder is of a specific type. Like `member` that we used in the previous example is of type [`Member`](../placeholders/member.md)\
and this type provides some useful information about the User and not just `mentions` the User\
Let's say you don't want to mention the User actually but just want to print the name of that User
After checking [`Member`](../placeholders/member.md) page, you will find there's exactly a property called `name` that does this so the message will be:
```
Hi <member name>
```
![](https://i.imgur.com/4GXfMnz.gif)

## More Examples
Almost all examples use placeholders\
Click [Here](../examples/) To see examples
