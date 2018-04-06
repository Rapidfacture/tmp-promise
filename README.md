# with-tmp-dir
Run a promise-based function with a temporary directory, deleting it afterwards.

Requires NodeJS 8+.

# Installation

```sh
npm install --save with-tmp-dir
```

# Usage example

```js
WithTempDir(function (tmpdir) {
    // tmpdir is a string like '/tmp/q3q235',
    // pointing to an existing temporary directory

    // Your code goes here

    // When this function returns, the tmp directory will be deleted
    // Remember to return a Promise here!
    return Promise.resolve("foobar"); // Example
}).then(function(arg) {
    // arg === 'foobar'

    // tmpdir, including all files in the directory,
    // is deleted here
});
```
