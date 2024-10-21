## Table of Contents
1. [Introduction to Express JS](#introduction-to-express-js)
2. [Installation](#installation)

<br>

## Introduction to Express JS
**Express JS** is Node JS framework. **Node JS** is a runtime environment that allows you to execute JavaScript code on the server side. It is built on Chrome's V8 JavaScript engine and enables developers to build scalable and high-performance applications, particularly **web servers** and **APIs**. 

<br>

## Installation
With **npm**
```cmd
npm install express --save
```
With **yarn**
``` cmd
yarn add express
```

<br>

If using npm installation, run this:
``` cmd
npm init
```
If using yarn installation, run this:
``` cmd
yarn init
```

<br>

## Getting started

Let's get started by this code.

**index.js**
``` javascript
const express = require('express')
const app = express()
app.get('/', (req, res) => res.send('Hello World!'))
app.listen(3000, () => console.log('Server ready'))
```

To run it, type `node index.js` on terminal
