# [⇦](/README.md)

# Initialize vanilla JS project (with ESLint and Jest)

**To initialize vanilla JS project without frameworks follow these steps:**

**1)** Initialize the project to generate a `package.json` file in your project's root directory:

```
npm init --yes
```

This file will contain information about your project, such as the name, version, and description.

**2)** Install **ESLint** as a development dependency:

```
npm install --save-dev eslint
```

**3)** Add an `.eslintrc.js` file in one of the supported configuration file formats, and configure it according to your needs.

Here's an example configuration:

```
module.exports = {
  "env": {
    "browser": true,
    "es2021": true,
    "node": true
  },
  "extends": "eslint:recommended",
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
}
```

**4)** Install **Jest** and `eslint-plugin-jest` as development dependencies:

```
npm install --save-dev jest eslint-plugin-jest
```

**5)** Update the `package.json` file to include the necessary scripts for running **ESLint** and **Jest**.

(*Npm scripts* are defined in your `package.json` file and can be run with the command `npm run your_script_name`.)

Add the following scripts under the scripts section:

```

...

"scripts": {
  "lint": "eslint .",
  "test": "jest"
}

...

```

**6)** Add `.gitignore`:

```
echo "node_modules" >> .gitignore
```

**7)** Add `README.md`:

```
echo "# author/project" >> README.md
```

___

Now you have a vanilla JS project set up with **ESLint** and **Jest**.
You can run `npm run lint` to lint your code and `npm run test` to run your tests.
