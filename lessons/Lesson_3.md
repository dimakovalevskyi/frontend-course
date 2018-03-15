# Node.js ecosystem, npm, bundlers

---

## What is Node.js ?

## What is npm ?

### package.json and package-lock.json

Basic structure of `package.json` file:

```
{
    "name": "My awesome project",
    "author": "Awesome I",
    "description": "My very cool and awesome project, best of the best.",
    "licence": "MIT",
    "private": false,
    "repository": {
        "type": "git",
        "url": "https://githib.com/awesome_i/my-awesome-project"
    },
    "scripts": {
        "build": "grunt build",
        "deploy": "some script for deploying on production"
    },
    "dependencies": {
        "express": "^1.0.1"
    },
    "devDependencies": {
        "grunt": "^1.0.1",
        "grunt-contrib-concat": "^1.0.1"
    }
}

```

### npm commands

 * `npm init`
 * `npm install` or `npm i`
 * `npm install --flags pckg-name`
 * `npm unstall --flags pckg-name`

## Ecosystem Node.js for frontend developers

## Bundlers

 * [Grunt](https://gruntjs.com/)
 * [Gulp](https://gulpjs.com/)
 * [Webpack](https://webpack.js.org/)
 * [Parcel](https://parceljs.org/)
