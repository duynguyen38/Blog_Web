# Blog_Web

## Create node.js

```bash
npm init
```

## Tutorial web: express.js

```bash
npm install express
```

## Install nodemon

```bash
npm install i nodemon --save-dev
```

## Vào package.json => mục script, thêm vào:

```bash
"start": "nodemon index.js"
or nodemon --inspect index.js
```

(dùng để debug)

## install morgan (dùng để nhìn log của web)

ADD:

```bash
npm install morgan
const morgan = require('morgan')
app.use(morgan('combined'))
```

---------------------------------------------
# template engine (handlebars)
## install
```bash
npm install express-handlebars
```

```bash
const path = require('path')
const { engine } = require('express-handlebars')
app.engine(
  "hbs",
  engine({
    extname: ".hbs",
  })
);
app.set('view engine', 'handlebars')
app.set('views', path.join(__dirname, 'resources/views'))
```
## Tạo folder 
/src/resources/scss, layout, views

	views/layouts/main.hbs (dùng lệnh ! ->tab)

	views/home.hbs
	views/news.hbs

	views/partials/header.hbs & footer.hbs