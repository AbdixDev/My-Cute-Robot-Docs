# User Join
Starts the sketch When user just joined your server

## Inputs
This starter doesn't need an input

## Placeholders
This starter provide a placeholder about the user who joined

#### Type
Member

#### Example
To get the user name that joined the server
```
:member name:
```

## Example of using this starter
### Welcomer Sketch
1- Make a sketch with starter `User Join`\
2- As first step select `Message` category, `Send` step\
3- Select the channel where you want to welcome the user\
4- As message you can use the placeholder to get the user name like:
```
Welcome :member username: to our server!
``` 
5- Save, and when user join your server, example `Abdi#1234`, the bot will send to welcome channe:
```
Welcomer Abdi to our server
```