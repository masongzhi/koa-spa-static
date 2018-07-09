# koa-spa-static
用于koa部署单页面资源（仅推荐使用在 `文档`，`mock`等 dev 服务）

## Requirements
[koa 2.x](https://github.com/koajs/koa)

## Installation

```bash
$ npm install koa-spa-static
```

## Options

 - `matchReg` Regex of matching front-end pages
 - `staticReg` Regex of matching front-end static. Defaults to "/static"
 - `root` [koa-static root](https://www.npmjs.com/package/koa-static) root
 - `opts` [koa-static opts](https://www.npmjs.com/package/koa-static#options) options

## Example

```js
import koa from 'koa'
import spaStatic from 'koa-spa-static'
const app = koa()

app.use(spaStatic({
  matchReg: /[^/api]|\//,
  root: path.join(__dirname, './dist'),
}));

app.listen(3000)

console.log('listening on port 3000');
```

