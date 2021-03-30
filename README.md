[![Youtube][youtube-shield]][youtube-url]
[![Facebook][facebook-shield]][facebook-url]
[![Instagram][instagram-shield]][instagram-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/learnwithsumit/nodejs-basic-bangla">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">সহজ বাংলায় Node.js টিউটোরিয়াল সিরিজ</h3>

<!-- TABLE OF CONTENTS -->

## Table of Contents

- [Update Node](#update-node)
  - [Windows](#windows)
  - [Mac](#mac)
- [Install and Update Yarn](#install-and-update-yarn)
  - [Windows](#on-windows)
  - [Mac](#on-mac)
- [VS Code Editor Setup](#vs-code-editor-setup)
  - [Extensions](#extensions)
  - [Settings](#settings)
  - [Set Line Breaks](#set-line-breaks)
- [Linting Setup](#linting-setup)
  - [Install Dev Dependencies](#install-dev-dependencies)
  - [Setup Linting Configuration file](#setup-linting-configuration-file)
- [Contact](#contact)

<!-- UPDATE NODE -->

## Update Node

Please follow the below instructions to update node in your machine:

### Windows

1. Update npm
   ```sh
   npm install npm@latest -g
   ```
2. Clear npm cache
   ```sh
   npm cache clean -f
   ```
3. Install n
   ```sh
   npm install -g n
   ```
4. Update node to latest version
   ```sh
   n latest
   ```

### Mac

1. With Homebrew
   ```sh
   brew update
   brew upgrade node
   ```

<!-- INSTALL & UPDATE YARN -->

## Install and Update yarn

Please follow the below instructions to install or update yarn in your machine.

### On Windows

1. Install yarn
   ```sh
   npm install -g yarn
   ```
2. Update yarn
   ```sh
   yarn set version latest
   ```

### On Mac

1. Install yarn
   ```sh
   brew install yarn
   ```
2. Update yarn
   ```sh
   brew update
   brew upgrade yarn
   ```

<!-- EDITOR SETUP -->

## VS Code Editor Setup

In order to follow along the tutorial series, I recommend you to use Visual Studio Code Editor and install & apply the below extensions and settings.

### Extensions

Install the below extensions:

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Path Autocomplete](https://marketplace.visualstudio.com/items?itemName=ionutvmi.path-autocomplete)

### Settings

Go to your Visual Stuido Code `settings.json` file and add the below settings there:

```json
// config related to code formatting
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.formatOnSave": true,
"[javascript]": {
  "editor.formatOnSave": false,
  "editor.defaultFormatter": null
},
"editor.codeActionsOnSave": {
  "source.fixAll.eslint": true,
  "source.organizeImports": true
},
"eslint.alwaysShowStatus": true
```

### Set Line Breaks

Make sure in your VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed). To do that, just click LF/CRLF in bottom right corner of editor, click it and change it to "LF". If you dont do that, you will get errors in my setup.

<img src="images/line-feed.jpg" alt="Line Feed" width="700">

<!-- LINTING SETUP -->

## Linting Setup

In order to lint and format your code automatically according to popular airbnb style guide, I recommend you to follow the instructions as described in video. References are as below.

### Install Dev Dependencies

```sh
yarn add -D eslint prettier
npx install-peerdeps --dev eslint-config-airbnb-base
yarn add -D eslint-config-prettier eslint-plugin-prettier
```

### Setup Linting Configuration file

Create a `.eslintrc.json` file in the project root and enter the below contents:

```json
{
  "extends": ["prettier", "airbnb-base"],
  "parserOptions": {
    "ecmaVersion": 12
  },
  "env": {
    "commonjs": true,
    "node": true
  },
  "rules": {
    "no-console": 0,
    "indent": 0,
    "linebreak-style": 0,
    "prettier/prettier": [
      "error",
      {
        "trailingComma": "es5",
        "singleQuote": true,
        "printWidth": 100,
        "tabWidth": 4,
        "semi": true
      }
    ]
  },
  "plugins": ["prettier"]
}
```

<!-- CONTACT -->

## Contact

Sumit Saha - [sumit@learnwithsumit.com](mailto:sumit@learnwithsumit.com)

Project Link: [https://github.com/learnwithsumit/nodejs-basic-bangla](https://github.com/learnwithsumit/nodejs-basic-bangla)

Youtube Channel: [https://youtube.com/LearnwithSumit](https://youtube.com/LearnwithSumit)

<!-- MARKDOWN LINKS & IMAGES -->

[youtube-shield]: https://img.shields.io/badge/-Youtube-black.svg?style=flat-square&logo=youtube&color=555&logoColor=white
[youtube-url]: https://youtube.com/LearnwithSumit
[facebook-shield]: https://img.shields.io/badge/-Facebook-black.svg?style=flat-square&logo=facebook&color=555&logoColor=white
[facebook-url]: https://facebook.com/letslearnwithsumit
[instagram-shield]: https://img.shields.io/badge/-Instagram-black.svg?style=flat-square&logo=instagram&color=555&logoColor=white
[instagram-url]: https://instagram.com/learnwithsumit
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/company/learnwithsumit
