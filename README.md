argg
====
A poor man's test runner for [tap](https://github.com/isaacs/node-tap), [tape](https://github.com/substack/tape), or similar, that also can be used with [istanbul](https://github.com/gotwarlost/istanbul). It's just three lines of code to `require` all globs or pathnames provided as command line arguments.

usage
-----
Install like:

    npm i argg  --save-dev

…then in your package.json add:

    "scripts": {
        "test": "node node_modules/argg tests/*.js",
        "cover": "istanbul cover node_modules/argg tests/*.js"
    },

…so from the command line, you do:

    npm test
    npm run cover

Sure, it barely deserves to be a module, but I got tired of copy/paste. Yes, tap has a [nice test runner](https://github.com/isaacs/node-tap/blob/master/lib/tap-runner.js) but I'd still need something [like this](https://github.com/substack/tape/pull/19) for tape and/or istanbul.

license
-------
MIT licensed by permission from my employer. See LICENSE.txt.
