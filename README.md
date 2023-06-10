## REMOVE Vietnamese Tones
```js
function removeVietnameseTones(text) {
  return text.normalize("NFD").replace(/[\u0300-\u036f]/g, "");
}
```

## SLUG
```js
function slug(text) {
  return text.normalize("NFD").replace(/[\u0300-\u036f]/g, "").toLowerCase().replace(/[^\w\s]/gi, "").replace(/\s+/, '-');
}
```

## Giới hạn text
```js
function limitWordCount(text, limit) {
  let words = text.trim().split(/\s+/);
  if (limit < words.length) {
    return words.slice(0, limit).join(' ') + '...';
  }
  return text;
}
```
