### webpack 打包封装js库
仅供个人学习参考使用

#### 依赖
```js
  "webpack": "^5.75.0"
  "webpack-cli": "^5.0.1"
```
#### 命令
```bash
  npm run build
```
相关配置（webpack.config.js）
```js
const path = require('path');

module.exports = {
    mode: "production",
    entry: './src/index.js',
    output: {
        path: path.resolve(__dirname, 'dist'),
        filename: 'ObjExtraFunctions.js',
        library: {
            name:'ObjExtraFunctions',   // 导出的模块名
            type:'umd'                  // 通用类型 建议
        }
    },
};
```


[参考教程](https://webpack.docschina.org/guides/author-libraries/)