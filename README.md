# swagger-js-codegen-template-typescript-fetch

These are templates for use with the project
[swagger-js-codegen](https://github.com/wcandillon/swagger-js-codegen).

They are used to generate a client which relies on the `fetch` browser api.

## Installation

### Requirements
* npm or yarn

`$ npm install --save-dev swagger-js-codegen-template-typescript-fetch`

or

`$ yarn add --dev swagger-js-codegen-template-typescript-fetch`

## Usage

```js
const templates = [
  "class",
  "definition",
  "method",
  "type"
].reduce((acc, name) => {
  acc[name] = fs.readFileSync(
    path.resolve(
      __dirname,
      `../node_modules/swagger-js-codegen-template-typescript-fetch/${name}.mustache`
     )
  );
  return acc;
}, {});

const source = Codegen.getCustomCode({
  className: "Api",
  swagger: spec,
  template
  /* , lint: false */
});
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[Apache 2.0](http://www.apache.org/licenses/)
