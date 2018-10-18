# JSEpisodeFour-Demo

[Slides]()

---

### Code Blocks (Objects)

BLOCK 01 (OBJECT STRUCTURE)

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
  name: "Hamsa",
  age: 45,
  interests: ["coding", "writing code", "reading documentation"],
  githubAccount: {
    username: "DarthHamza",
    numberOfRepos: 1000000
  },
  greeting: function() {
    console.log("Hello!");
  }
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
person.name = "Mshary";
person.interests.push("Intense Introspection");
person.githubAccount.username = "DarkWight";
person.greeting();
```
