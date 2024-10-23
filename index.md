## Table of Contents
1. [Introduction to Express JS](#introduction-to-express-js)
2. [Installation](#installation)
3. [Getting Started](#getting-started) 

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

To run it, type `node index.js` on terminal to start the server.

On the first line, we import `express` package on `express` variable. 
<br>
On the second line, we instantiate an application by calling its `app()` method on `app` variable. `app()` is like `createServer()` in Node JS.
<br>
After we have the application object, we tell it to `GET` data as a response to request from path `/`, using `get()` method.
<br>
<br>
There is a method for every HTTP verb: `get()`, `post()`, `put()`, `delete()`, `patch()`:
``` javascript
app.get('/', (req, res) => { /* */ })
app.post('/', (req, res) => { /* */ })
app.put('/', (req, res) => { /* */ })
app.patch('/', (req, res) => { /* */ })
app.delete('/', (req, res) => { /* */ })
```
`get()` is used to **get** data from API.
<br>
`post()` is used to **send** data to API.
<br>
`put()` and `patch()` are used to **update** data on API.
<br>
`delete()` is used to **delete** data from API.
<br>

**Differences between put() and patch()**
<br>
`put()` is used to update the **entire** record, while `patch()` only updates **partially**.

<br>
Those methods accept a callback function, which is called when a request is started, and we
need to handle it.
<br>

We pass in an arrow function:
``` javasscript
(req, res) => res.send('Hello World!')
```
abc
