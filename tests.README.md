I wrote tests to help me complete the assignments correctly. It was unnecessary but lol why not :)
TO use the tests.
step 1 run the following command in your terminal in the project folder.
```
npm install
npm install babel-core
```

paste the following code in your helper.js located in `/test` folder
```Js
const chai = require('chai')
global.expect = chai.expect
const fs = require('fs')
const jsdom = require('mocha-jsdom')
const path = require('path')
const babel = require('babel-core');

const html = fs.readFileSync(path.resolve(__dirname, '..', 'index.html'), 'utf-8')

const babelResult = babel.transformFileSync(
  path.resolve(__dirname, '..', 'src/00-objectball.js'), {
    // presets: ['env']
  }
);

const src = babelResult.code

jsdom({
  html, src
});
```
Copy the code at the `indexTest.js` located at `/test` folder and replace the existing coce

Yes it was brutal!!
## Happy Coding