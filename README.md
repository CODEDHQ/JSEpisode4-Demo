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
person.name = "Hamsa";
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
