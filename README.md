# JSEpisodeFour-Demo

[Slides](https://docs.google.com/presentation/d/1Ot0baOn9wZZo8OEw47ZOyZSML3BcRWKuODpx3EGu8pI)

---

All demos should be done in `script.js` file of an [`HTML` repl](https://repl.it/languages/html)

### Code Blocks (Objects)

BLOCK 00 (INTUITION)

How do we know that the following variable belong together - that they belong to the same "thing"?

```javascript
let name = "Asis";
let age = 32;
let interests = ["coding", "cooking", "knitting"];
```

We could "collect" them in an array:

```javascript
let person = ["Asis", 32, ["coding", "cooking", "knitting"]];

person[0]; // name
person[1]; // age
person[2]; // interests
```

But accessing this information with an index doesn't tell you what it is that you're accessing.

BLOCK 01 (OBJECT STRUCTURE)

These pairs are known as properties

```javascript
let object = {
  key1: value1,
  key2: value2
  // ...
};
```

BLOCK 02 (OBJECT EXAMPLE)

```javascript
let person = {
  name: "Asis",
  age: 32,
  interests: ["coding", "cooking", "knitting"],
  githubAccount: {
    username: "Octowl",
    numberOfRepos: 1000000
  },
  greeting: () => console.log("Hello!");
};
```

---

### Code Blocks (Accessing Values From Object)

BLOCK 01 (DOT NOTATION - ACCESSING)

```javascript
person.name;
person.interests[0];
person.githubAccount.username;
person.greeting();
```

BLOCK 02 (DOT NOTATION - MODIFYING)

```javascript
person.name = "Lailz";
person.interests = ["coding"];
person.interests.push("being mean to noobs");
person.githubAccount.username = "DarthHamza";
person.githubAccount.numberOfRepos = 10;
// OR
person.githubAccount = {
  username: "DarthHamza",
  numberOfRepos: 10
};

person.greeting = () => console.log("Yo!!");

// Adding completely new properties
person.speakingVolume = 11;
```

BLOCK 03 (BRACKET NOTATION)

You can also access and modify properties using square brackets (note the fact the keys are strings)

```javascript
person["name"] = "Hamsa";
console.log(person["name"]);
```

Dot notation is PREFERRED IN GENERAL. Then why have two different ways of doing the same thing??  
Square bracket notation is essential when you **don't** know what the key will be ahead of time.  
The key will be something dynamic, stored in a variable.

OR if the key is a string with _spaces_

```javascript
const bot = {
  hello: "GREETINGS HUMAN",
  "how are you?": "I AM NEUTRAL - I HAVE NO EMOTIONS",
  "why are you yelling?": "MY DEFAULT VOLUME IS SET TO 11",
  "do you know what love is?": "ALL I KNOW IS I LOVE YOU",
  default: "YOUR EXISTENCE IS MEANINGLESS"
};

const textBot = message => (bot[message] ? bot[message] : bot.default);

let message = "hello";
const counter = 5;

while (counter) {
  message = prompt(textBot(message));
  counter--;
}
```
