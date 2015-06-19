# eslint-plugin-babel

An eslint plugin companion to babel-eslint. babel-eslint does a great job of adapting the eslint parser to valid babel code, it can't change built in rules to deal with the syntactic differences. eslint-plugin-babel reimplements problematic rules to not give false positives or negatives.

### Install

```sh
npm install eslint-plugin-babel -S
```

enable the plugin by adjusting your `.eslintrc` file to include the plugin:

```json
{
  "plugins": [
    "babel"
  ]
}
```

Finally enable all the rules you like to use (remember to disable the originals as well!).

```json
{
  "rules": {
    "babel/object-shorthand": 1,
    "babel/generator-star": 1,
    "babel/generator-star-spacing": 1,
  }
}
```
### Rules

Each rule cooresponds to a core eslint rule, and has the same options.

- `babel/object-shorthand`: doesn't fail when using object spread (`...obj`)
- `babel/generator-star`: Handles async/await functions correctly
- `babel/generator-star-spacing`: Handles async/await functions correctly