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

```
touch .eslintrc.js
```

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

Add the following scripts under the *scripts* section:

```

...

"scripts": {
  "lint": "eslint .",
  "test": "jest"
}

...

```

**6)** Add `index.html`:

```
touch index.html
```

```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <link rel="stylesheet" href="styles.css" />

  <title></title>
</head>

<body>
  <script type="module" src="./index.js"></script>

  <header></header>
</body>
</html>

```

**7)** Add `index.js`:

```
touch index.js
```

**8)** Add `styles.css`:

```
touch styles.css
```

```
:root {
  --bg: #ebe6f0;
  --fg: #22181c;
  --alt-fg: #7a79b7;
  --alt-bg: #00afb5;
  --font-size: 20px;

  background-color: var(--bg);
}

@font-face {
  font-family: "Iosevka";
  src: url("src/assets/fonts/iosevka-light.woff2") format("woff2");

  font-stretch: normal;
  font-style: normal;
}

* {
  margin: 0;
  padding: 0;
}

h1 {
  font-weight: 500;
  text-align: center;
}

body {
  font-family: Iosevka, sans-serif;
  font-size: var(--font-size);
  text-align: left;
  color: var(--fg);
  min-height: 100%;
}

```

**9)** Add font-family to `src/assets/fonts/`:

```
mkdir -p src/assets/fonts
```

[ayveezub/com-sci-pills/assets/fonts](https://github.com/ayveezub/com-sci-pills/tree/main/assets/fonts)

**10)** Add `.gitignore`:

```
echo "node_modules" >> .gitignore
```

**11)** Add `README.md`:

```
touch README.md
```

___

Now you have a vanilla JS project set up with **ESLint** and **Jest**.
You can run `npm run lint` to lint your code and `npm run test` to run your tests.
