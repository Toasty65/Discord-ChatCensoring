# ChatCensoring

A tiny & simple package for your `chat application` that allows you to `remove` or `censor` bad words in chat.

# Installation 

### [npm](https://docs.npmjs.com/cli/v6/commands/npm): ###

`npm i chat-censoring`

# Features

- Check. if a message includes bad words
- Check **and** censor (if needed) a message

## Check message

This function takes your message as argument and checks, if it includes a bad word. As result it returns either true or false.

**Parameters:**

Parameter|Usage
---------|-----
message|The message you want to check


**Example:**

```js
const censoring = require('chat-censoring');

const isInsult = censoring.check('You are great!');
console.log(isInsult); // Prints false
```

```js
const censoring = require('chat-censoring');

const isInsult = censoring.check('You are fucking stupid!');
console.log(isInsult); // Prints true
```

## Censor message

This function checks if there is a bad word in your provided message and replaces this word(s) with the character of your choise.

**Parameter:**

Parameter|Usage
---------|-----
message|The message you want to check **and** censor if needed
censoringChar|The char you want to use to censor bad words

**Example:**

```js
const censoring = require('chat-censoring');

const friendlyMessage = censoring.censorMessage('This is fucking cool!', '*');
console.log(friendlyMessage); // Prints 'This is ******* cool!'
```