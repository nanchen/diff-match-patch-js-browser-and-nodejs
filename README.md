# diff-match-patch-js-browser-and-nodejs

npm package (browser and nodejs) for https://github.com/google/diff-match-patch/javascript

[![Build Status](https://img.shields.io/travis/JackuB/diff-match-patch/master.svg)](https://travis-ci.org/JackuB/diff-match-patch)
[![Dependency Status](https://img.shields.io/david/JackuB/diff-match-patch.svg)](https://david-dm.org/JackuB/diff-match-patch)
[![NPM version](https://img.shields.io/npm/v/diff-match-patch.svg)](https://www.npmjs.com/package/diff-match-patch)
[![Known Vulnerabilities](https://snyk.io/test/github/JackuB/diff-match-patch/badge.svg)](https://snyk.io/test/github/JackuB/diff-match-patch) 

When importing the JS file from npm pacakge https://www.npmjs.com/package/diff-match-patch in a browser, it gives error: "Uncaught ReferenceError: module is not defined at index.js:2186", this motivated me to have this package.

## Installation

    npm install diff-match-patch-js-browser-and-nodejs

## API

[Source](https://github.com/google/diff-match-patch/wiki/API)

### Instructions

diff_match_uncompressed.js is the human-readable version. This should be used by developers and Node.js.

diff_match_patch.js has been compressed using Google's Closure Compiler on 'simple' mode. This reduces the size to 25% of the uncompressed version.

The JavaScript version has no dependencies. It works in Netscape 4, Internet Explorer 5.5, and all browsers released since the year 2000 (the limiting factor is the use of the encodeURI function).

Tests
Unit tests can be performed by pointing a web browser at javascript/tests/diff_match_patch_test.html. Over a hundred tests should run, with zero failures.

Speed test for diff can be performed by pointing a web browser at javascript/tests/speedtest.html and pressing "Compute Diff".

## Usage (Browser)
Hello World
Here's a minimal example of a diff in JavaScript:

<html>
  <body>
    <script src="diff_match_patch.js"></script>
    <script>
      var dmp = new diff_match_patch();
      var diff = dmp.diff_main('Hello World.', 'Goodbye World.');
      // Result: [(-1, "Hell"), (1, "G"), (0, "o"), (1, "odbye"), (0, " World.")]
      dmp.diff_cleanupSemantic(diff);
      // Result: [(-1, "Hello"), (1, "Goodbye"), (0, " World.")]
      alert(diff);
    </script>
  </body>
</html>
Save the above as an HTML file in the javascript directory, then open the file in any web browser.

## Usage (NodeJs)
To be done

## License

  http://www.apache.org/licenses/LICENSE-2.0
