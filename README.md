# v8flags [![Build Status](https://secure.travis-ci.org/js-cli/js-v8flags.png)](http://travis-ci.org/js-cli/js-v8flags) [![Build status](https://ci.appveyor.com/api/projects/status/9psgmwayx9kpol1a?svg=true)](https://ci.appveyor.com/project/js-cli/js-v8flags)
> Get available v8 flags.

[![NPM](https://nodei.co/npm/v8flags.png)](https://nodei.co/npm/v8flags/)

## Example
```js
const v8flags = require('v8flags');

v8flags(function (err, results) {
  console.log(results);  // [ '--use_strict',
                         //   '--es5_readonly',
                         //   '--es52_globals',
                         //   '--harmony_typeof',
                         //   '--harmony_scoping',
                         //   '--harmony_modules',
                         //   '--harmony_proxies',
                         //   '--harmony_collections',
                         //   '--harmony',
                         // ...
});
```

## Release History

* 2018-02-26 - v3.0.2 - fix typo in the failure message
* 2017-09-24 - v3.0.1 - fix home directory lookup behavior & fallback
* 2017-07-14 - v3.0.0 - store cached config to operating system specific directories
* 2017-04-18 - v2.1.1 - default to an empty user
* 2017-04-18 - v2.1.0 - hash username to support invalid path characters
* 2017-03-31 - v2.0.12 - don't pollute global namespace
* 2015-12-07 - v2.0.11 - cache to temp directory if home is present but unwritable
* 2015-07-28 - v2.0.10 - don't throw for electron runtime, just call back with empty array
* 2015-06-25 - v2.0.9 - call back with flags even if cache file can't be written
* 2015-06-15 - v2.0.7 - revert to 2.0.5 behavior.
* 2015-06-15 - v2.0.6 - store cache file in ~/.cache or ~/AppData/Local depending on platform
* 2015-04-18 - v2.0.5 - attempt to require config file, if this throws for any reason, fopen w+ and re-create
* 2015-04-16 - v2.0.4 - when concurrent processes are run and no config exists, don't append to the cached config.
* 2015-03-31 - v2.0.3 - prefer to store config files in user home over tmp
* 2015-01-18 - v2.0.2 - keep his dark tentacles contained
* 2015-01-15 - v2.0.1 - store temp file in `os.tmpdir()`, drop support for node 0.8
* 2015-01-15 - v2.0.0 - make the stupid thing async
* 2014-12-22 - v1.0.8 - exclude `--help` flag
* 2014-12-20 - v1.0.7 - pre-cache flags for every version of node from 0.8 to 0.11
* 2014-12-09 - v1.0.6 - revert to 1.0.0 behavior
* 2014-11-26 - v1.0.5 - get node executable from `process.execPath`
* 2014-11-18 - v1.0.4 - wrap node executable path in quotes
* 2014-11-17 - v1.0.3 - get node executable during npm install via `process.env.NODE`
* 2014-11-17 - v1.0.2 - get node executable from `process.env._`
* 2014-09-03 - v1.0.0 - first major version release
* 2014-09-02 - v0.3.0 - keep -- in flag names
* 2014-09-02 - v0.2.0 - cache flags
* 2014-05-09 - v0.1.0 - initial release
