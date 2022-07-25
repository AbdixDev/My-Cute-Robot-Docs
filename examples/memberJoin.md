# Welcomer
Let's see how our cute robot can welcome the newcomers in the server

## Goal
To welcome the new users in a channel (example: #welcome)
by sending message:
```
Welcome @user to our cute server
```

Only that? No. Let's also add role @member

![](https://i.imgur.com/VbIS3q0.jpg)

## Steps
1- Send `-create` in the server, and name the sketch `Welcomer` (it can be anything)\
![](https://i.imgur.com/H9Tpa4p.jpg)

2- Which Starter will we use?\
Obviously [`User Join`](../starters/memberJoin.md) starter\
![](https://i.imgur.com/ebzwUok.jpg)

3- Now, what will our first step be? Let's send the message by choosing: `Message` then `Send`\
![](https://i.imgur.com/6f6372z.jpg)

4- Select the channel where it will send (#welcome). Then let's tell the bot what is the message\
![](https://i.imgur.com/1G7MvAj.jpg)\
**Note**: we used a [placeholder](../tutorials/placeholder.md) of [member](../placeholders/user.md) provided by the [starter](../starters/memberJoin.md)

5- Then let's add our 2nd step, which is, to add the role. Select `Role` then `Give`\
![](https://i.imgur.com/ljKooh1.jpg)\
![](https://i.imgur.com/3aKMlPm.jpg)

6- Bot will ask, `give role to which User?`, of course the `Joined member`\
![](https://i.imgur.com/MiSXLxu.jpg)

7- Which role? Let's pick `Member`\
![](https://i.imgur.com/pechlZI.jpg)

8- Save, and that looks neat\
![](https://i.imgur.com/JHpP58b.jpg)

## Result
When a user join the server

![](https://i.imgur.com/VbIS3q0.jpg)
