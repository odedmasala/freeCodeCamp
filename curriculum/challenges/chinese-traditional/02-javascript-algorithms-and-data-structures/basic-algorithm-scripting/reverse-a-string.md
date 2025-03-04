---
id: a202eed8fc186c8434cb6d61
title: 反轉字符串
challengeType: 1
forumTopicId: 16043
dashedName: reverse-a-string
---

# --description--

Reverse the provided string and return the reversed string.

For example, `"hello"` should become `"olleh"`.

# --hints--

`reverseString("hello")` should return a string.

```js
assert(typeof reverseString('hello') === 'string');
```

`reverseString("hello")` should return the string `olleh`.

```js
assert(reverseString('hello') === 'olleh');
```

`reverseString("Howdy")` should return the string `ydwoH`.

```js
assert(reverseString('Howdy') === 'ydwoH');
```

`reverseString("Greetings from Earth")` should return the string `htraE morf sgniteerG`.

```js
assert(reverseString('Greetings from Earth') === 'htraE morf sgniteerG');
```

# --seed--

## --seed-contents--

```js
function reverseString(str) {
  return str;
}

reverseString("hello");
```

# --solutions--

```js
function reverseString(str) {
  return str.split('').reverse().join('');
}

reverseString("hello");
```
