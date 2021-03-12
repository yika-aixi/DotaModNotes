#### 1. `package.json`添加

- 需要注意将第二个路径修改为自己目录路径

```
{
  "scripts": {
    "build": "node --preserve-symlinks node_modules/webpack/bin/webpack.js --config content/panorama/xxx/xxx/webpack.config.js",
    "dev": "node --preserve-symlinks node_modules/webpack/bin/webpack.js --config content/panorama/xxx/xxx/webpack.config.js --watch"
  }
}
```

#### 2. 使用命令 `node --preserve-symlinks node_modules/webpack/bin/webpack.js`

#### 3. 使用命令 `npm install -D webpack@next webpack-cli webpack-panorama`

#### 4. 创建文件 `webpack.config.js`,路径在第一步第二个参数,并复制下面内容保存,注意需要修改被我添加了`xxx`的路径为具体需要处理合并的目标,路径都是相对于`webpack.config.js`

```
const path = require('path');
const { PanoramaTargetPlugin } = require('webpack-panorama');
/** @type {import('webpack').Configuration} */
module.exports = {
  entry: {
    hud: './hud/xxx/script.js',
  },

  mode: 'development',
  context: path.resolve(__dirname, 'src/xxx/'),
  output: {
    path: path.resolve(__dirname, 'scripts/xxx/custom_game'),
  },

  resolve: {
    // Required because of reverse symlinking
    symlinks: false,
  },

  plugins: [new PanoramaTargetPlugin()],
};
```

![image](https://user-images.githubusercontent.com/22412994/110927336-5d04a900-82da-11eb-97cb-e259e3e3a7a8.png)

![image](https://user-images.githubusercontent.com/22412994/110927415-74439680-82da-11eb-97d9-778daf9ac67d.png)


#### 5. 执行命令 `npm run build` 看是否有错,没错就开启Watch(`npm run dev`)



---------------------------------------------------------------------------------------------------------------------------------------------------


### 安装第三方库 : https://moddota.com/panorama/webpack/#loaders-and-typescript ---- [ts](https://moddota.com/panorama/webpack/#typescript)

- 安装好以后编辑`webpack.config.js`的`module`块
- ts注意最后编辑的`tsconfig.json`文件的`include`值为具体的目录名

![image](https://user-images.githubusercontent.com/22412994/110929412-c685b700-82dc-11eb-8e7b-4b71e9966457.png)


