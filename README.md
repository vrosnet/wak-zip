wak-zip
=======

Wakanda module to zip and unzip files and folders.

About
-----

* libboost/1.57.0
* libz/1.28

Example
-------
```js
var modulesFolder = FileSystemSync('Modules');
var zip = require(modulesFolder.path + 'zip');

var desktop = FileSystemSync('Desktop').path;

var input = desktop + "sample";
var output = desktop + "test.zip";
var level = 0;//default, 1-9
var ignoredotfile = true;
var verbose = false;

zip.zip(input, output, level, ignoredotfile, verbose);

input = output;
output = desktop + "test";

zip.unzip(input, output, level, verbose);

```
**Note**: Unicode file paths are supported on all platforms. You can ignore dot files and dot folders for both archiving and extracting. Specifying the verbose option will list all relative paths in stdOut.


