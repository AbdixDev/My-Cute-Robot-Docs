# User Say Something
Starts the sketch When user send a message

## Inputs
This starter requires 1 input, which is text that message must starts with

## Placeholders
This starter provide 3 placeholders about the user, the message and the channel where he sent in

#### User
The member who started the sketch
##### Example
To get the user name
```
:member name:
```

#### Message
The user message which started the sketch
##### Example
To get the message content
```
:message:
```


## Example of using this starter
### Responder Sketch to ?hello
1- Make a sketch with starter `User Say Something`\
2- Send `?hello` as Starter input
3- As first step select `Message` category, `Send` step\
4- Select the channel where the sketch starter
5- As message you can use the placeholder to get the user name like:
```
Hello :member: ❤️
``` 
5- Save, and when user send a text starts with `?hello`, the bot will send:
```
Hello @user ❤️
```