# Test Modules Locally

Load a module from anywhere on your computer with `npm link`. An easy way to test the export/import of npm modules before publishing to npm.

## Getting Started

Clone this repo and cd into it

```
git clone git@github.com:melanieseltzer/test-modules-locally.git && cd test-modules-locally
```

Open a new terminal tab and cd to the module's folder that needs to be tested, then run `npm link`. This creates a global symlink.

```
cd path/to/module_name
npm link
```

Back in the `test-modules-locally` folder in terminal, run `npm link <module_name>`. This creates a local symlink for testing.

## Usage

To run the test, configure `index.js` to make use of your module somehow (e.g. console.log)

```
import foo from 'foo';
const test foo()
console.log(test)
```

Once this is configured, run the test script

```
npm run test
```

This transpiles and then executes the code in Node. If successful, you will see your `console.log` output in the terminal.

:tada: Your module is successfully importing!