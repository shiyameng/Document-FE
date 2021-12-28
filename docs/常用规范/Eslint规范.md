# ESLint 规范
更新时间：{docsify-updated}

## whyEslint

ESLint（https://eslint.org/） 是一款开源的 JavaScript lint 工具，由 Nicholas C. Zakas 于2013 年创建。
借助 ESLint，可将 静态代码分析 和 问题代码协助修复 集成到 编码、提交 和 打包 过程中，及早发现并协助修复代码中：

- 有语法错误的部分
- 不符合约定的样式准则的部分
- 不符合约定的最佳实践的部分

在项目开发中获得如下收益：

- 在执行代码之前发现并修复语法错误，减少调试耗时和潜在 bug
- 保证项目的编码风格统一，提高可维护性
- 督促团队成员在编码时遵守约定的最佳实践，提高代码质量


## 安装

yarn global add eslint

cd 项目

yarn add eslint --dev

eslint--init

项目均使用airbnb的规范，eslint会根据vue/react引入不同的插件。

#### 以react项目为例：

✔ How would you like to use ESLint? · style
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
✔ Does your project use TypeScript? · No / Yes
✔ Where does your code run? · browser, node
✔ How would you like to define a style for your project? · guide
✔ Which style guide do you want to follow? · airbnb
✔ What format do you want your config file to be in? · JavaScript
Checking peerDependencies of eslint-config-airbnb@latest
The config that you've selected requires the following dependencies:

eslint-plugin-react@^7.27.1 @typescript-eslint/eslint-plugin@latest eslint-config-airbnb@latest eslint@^7.32.0 || ^8.2.0 eslint-plugin-import@^2.25.3 eslint-plugin-jsx-a11y@^6.5.1 eslint-plugin-react-hooks@^4.3.0 @typescript-eslint/parser@latest
✔ Would you like to install them now with npm? · No / Yes
Installing eslint-plugin-react@^7.27.1, @typescript-eslint/eslint-plugin@latest, eslint-config-airbnb@latest, eslint@^7.32.0 || ^8.2.0, eslint-plugin-import@^2.25.3, eslint-plugin-jsx-a11y@^6.5.1, eslint-plugin-react-hooks@^4.3.0, @typescript-eslint/parser@latest


## 配置

- 用.eslintrc.js 文件导出一个包含配置信息的对象。
- 用.eslintignore 忽略某些配置的js文件。
- 在同一个项目中，不建议为不同目录指定不同的配置文件。
- 不允许注释内嵌配置，例如/*eslint-disable*/

### 配置参数

- env注意跟随标准更新
- 有需要更改的rules，需讨论后统一修改。

现有rules：

rules: {
    'react/function-component-definition': [2, { namedComponents: 'function-declaration' }],
    'react/jsx-filename-extension': [1, { extensions: ['.js', '.jsx', '.ts', '.tsx'] }],
    'react/jsx-one-expression-per-line': 'off',
},



## git commit 集成




## 其他
- 不推荐安装prettier，更不可用prettier覆盖eslint的规范。

