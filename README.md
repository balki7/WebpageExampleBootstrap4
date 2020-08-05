go to the file:

node_modules/parallelshell/index.js:105
Then change this line:

cwd: process.versions.node < '8.0.0' ? process.cwd : process.cwd(),
To this:

cwd: parseInt(process.versions.node) < 8 ? process.cwd : process.cwd(),