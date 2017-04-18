# npmdoc-publish-latest

#### api documentation for  [publish-latest (v1.1.2)](https://github.com/kentcdodds/publish-latest#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-publish-latest.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-publish-latest) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-publish-latest.svg)](https://travis-ci.org/npmdoc/node-npmdoc-publish-latest)

#### Script to publish generated files to a `latest` branch

[![NPM](https://nodei.co/npm/publish-latest.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/publish-latest)

- [https://npmdoc.github.io/node-npmdoc-publish-latest/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-publish-latest/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-publish-latest/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-publish-latest/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-publish-latest/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-publish-latest/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Kent C. Dodds",
        "url": "http://kentcdodds.com/"
    },
    "bin": {
        "publish-latest": "bin/publish-latest"
    },
    "bugs": {
        "url": "https://github.com/kentcdodds/publish-latest/issues"
    },
    "config": {
        "ghooks": {
            "commit-msg": "./node_modules/.bin/validate-commit-msg && npm run eslint && npm t && npm run check-coverage && echo 'pre-commit checks good 👍'"
        }
    },
    "czConfig": {
        "path": "node_modules/cz-conventional-changelog/"
    },
    "dependencies": {
        "commander": "^2.8.1",
        "parse-author": "0.2.0",
        "path-here": "^1.1.0",
        "repo-path-parse": "1.0.1"
    },
    "deprecated": "This is no longer necessary https://medium.com/@kentcdodds/why-i-don-t-commit-generated-files-to-master-a4d76382564",
    "description": "Script to publish generated files to a 'latest' branch",
    "devDependencies": {
        "babel": "5.8.23",
        "chai": "3.2.0",
        "chai-string": "1.1.2",
        "codecov.io": "0.1.6",
        "commitizen": "1.0.4",
        "cz-conventional-changelog": "1.1.0",
        "eslint": "1.4.1",
        "eslint-config-kentcdodds": "4.0.0",
        "eslint-plugin-mocha": "0.5.1",
        "ghooks": "0.3.2",
        "istanbul": "0.3.19",
        "lodash": "3.10.1",
        "mocha": "2.3.2",
        "semantic-release": "^4.3.4",
        "validate-commit-msg": "1.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "454a7849d364f497510a5f20bd99f17550b3a8f7",
        "tarball": "https://registry.npmjs.org/publish-latest/-/publish-latest-1.1.2.tgz"
    },
    "gitHead": "cf57c33e279f3149fad80d53bfc2d3071b4e92b9",
    "homepage": "https://github.com/kentcdodds/publish-latest#readme",
    "keywords": [
        "git",
        "ci",
        "release",
        "publish"
    ],
    "license": "MIT",
    "main": "dist/index.js",
    "maintainers": [
        {
            "name": "kentcdodds"
        }
    ],
    "name": "publish-latest",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/kentcdodds/publish-latest.git"
    },
    "scripts": {
        "build": "cd src && babel index.js -d ../dist && cd ..",
        "check-coverage": "istanbul check-coverage --statements 80 --branches 58 --functions 90 --lines 80",
        "commit": "git-cz",
        "eslint": "eslint src/ -c other/src.eslintrc --ignore-path other/src.eslintignore && eslint src/*.test.js",
        "postpublish": "bin/publish-latest",
        "prebuild": "rm -rf dist && mkdir dist",
        "prepublish": "npm run build",
        "report-coverage": "cat ./coverage/lcov.info | codecov",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "start": "npm run test:watch",
        "test": "istanbul cover -x *.test.js _mocha -- -R spec src/index.test.js --compilers js:babel/register",
        "test:watch": "mocha src/*.test.js -w --compilers js:babel/register"
    },
    "version": "1.1.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
