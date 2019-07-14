# 002. Pin Down NPM Package Versions with Yarn.lock

Video: https://egghead.io/lessons/npm-pin-down-npm-package-versions-with-yarn-lock

npm shrinkwrap > npm install > npm shrinkwrap is not guaranteed to produce the same output as just shrinkwrapping once, whereas Yarn explicitly uses "an install algorithm that is deterministic and reliable". We’ll learn how to generate a yarn.lock file and commit it to version control to ensure a deterministic and reliable module install process.

## Transcript:

By default, NPM is not 100 percent deterministic. Even if you use NPM shrinkwrap, you cannot guarantee that what you NPM install on one computer will NPM install exactly the same on another computer. You can fix this by using Yarn.

Yarn was built to be deterministic, reliable, and fast. New projects can get started very easily by typing "yarn add" followed by the package you want to install. You can also specify an exact version to install, or use a range or version constraint if you prefer a different install criteria.

After installing the first package, yarn will create a yarn.lock file. We can check the exact pin-down version of this package by searching for our installed package in this file. Yarn also does file checks on matches to ensure exact one-to-one downloaded results.

Regarding version control, be sure to add both the package.json file and the yarn.lock file to your repository. You'll also want to ignore the node modules directory, as these assets are compiled when the yarn command is ran later at bill time, or post deploy.
