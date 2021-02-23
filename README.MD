# L04 Transpiler Babel

> Using Babel to transpile and polyfill

As a Javascript Developer, I want to target the latest ES features while maintaining browser compatibility, so that I can code fast but support older browsers


This code is based off this article [Why you don’t need Babel](https://blog.logrocket.com/why-you-dont-need-babel/)

## Before and After

Before and after for L04 Transpiler Babel in HTML

<table>
<tr>
  <th>Before</th>
  <th>After</th>
</tr>
<tr>
  <td>
  
  ![Before](shot-before.png 'Before screenshot')
  
  </td>
  <td>
  
  ![After](shot-after.png 'After screenshot')
  
  </td>
</tr>
</table>

## Development

Run `node dist/test.js` from command line

```bash
# cd [YouCustomDevFolder]
git clone git@github.com:klueless-html-samples/L04TranspilerBabel.git && cd L04TranspilerBabel

npm install

# Run the transpiler
npx babel src --out-dir dist --presets=@babel/env

# Run the code
node dist/test.js

# NOTE: There should be no assertion errors, but it will say fetch is not defined since Node.js has no fetch() method. 
```

## Code Setup

```bash
# Setup Transpilers for ES6 support
npm install --save-dev @babel/core @babel/cli @babel/preset-env
npm install --save @babel/polyfill

```

Add the following to package.json.

```javascript
  "browserslist": [
    "defaults"
  ]
```

## License

The code is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Copyright

Copyright (c) David Cruwys. See [MIT License](LICENSE.txt) for further details.
