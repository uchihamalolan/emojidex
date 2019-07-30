# Emojidex
[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)


> comprehensive list of all emojis along with their properties

**NOTE**: The lists is related with the Unicode Hex Character Code. The representation of the emoji depend of the system. Will be possible that the system don't have all the representations.

## Installation

Use the npm to install emojidex.

```zsh
npm install @uchihamalolan/emojidex
```

## Usage

```js
const { emojidata, emojilist } = require('emojidex')
console.log(emojidata['people'][0])

// output => 
{ 
  codes: '1F600',
  char: '😀',
  name: 'grinning face',
  category: 'Smileys & Emotion',
  subcategory: 'face-smiling',
  keyTerms: [ 'face', 'grin', 'grinning face' ] 
}
```

## Properties
`emojidata` object consist of all emojis along with their properties.

`emojilist` object consist of just emojis grouped by their categories.

**NOTE**: You can flatten `emojilist` object if you require just an array of emojis.

### Sample content of `emojidata`
```js
emojidata = {
  "people": [
            { codes: '1F600',
              char: '😀',
              name: 'grinning face',
              category: 'Smileys & Emotion',
              subcategory: 'face-smiling',
              keyTerms: [ 'face', 'grin', 'grinning face' ] 
            },
            ...
          ],
  "nature": [...],
  "food": [...],
  "activity": [...], 
  "travel": [...], 
  "object": [...], 
  "symbol": [...], 
}
```
### List of category keywords to be used for parsing
- **people** for *Smileys & People*
- **nature** for *Animals & Nature*
- **food** for *Food & Drink*
- **activity** for *Activity*
- **travel** for *Travel & Places*
- **object** for *Objects*
- **symbol** for *Symbols*
- **flags** for *Flags*

### Content of an emoji object
- **codes** => list of unicodes of the emoji in a string, separated by spaces.
- **char** => emoji as a simple string.
- **name** => official name of the emoji.
- **category** => category into which the emoji belongs to.
- **subcategory** => subcategory into which the emoji belongs to.
- **keyTerms** => List of terms that can be used for search functionalities

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
