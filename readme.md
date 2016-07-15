# Angular 2 

### Testing

```bash

gulp test

```

Runs tests with [Karma](https://karma-runner.github.io/0.13/index.html) and [Jasmine](http://jasmine.github.io/).
Uses a single entry point (```setup.spec.js```), which includes all the ```*.spec.js``` files and runs the tests inside them.
The test files can be found in the ```client/app``` folder next to the source files.

Because a clean bundling with Webpack can take multiple seconds, it is not ideal for development to run a clean test run every time.
Instead it can run continuously on your development machine.

```bash

gulp test-dev

```

T
### Deployment (to Heroku)

It bundles the client application and copies static files and server files to the ```dist``` directory along with ```package.json```.
Then it can be commited to the desired location (for example Heroku).

```bash

gulp dist

cd dist
git init
git add -A .
git commit -m "Deploy #1" && echo Committed
git push -f git@heroku.com:angular2-es6-starter.git master

```

Check out the [deployed version](https://angular2-es6-starter.herokuapp.com/).
