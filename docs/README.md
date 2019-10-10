# House Platform





房产交易平台

## 环境和依赖

- node
- yarn
- webpack
- eslint
- @vue/cli ~3
- [ant-design-vue](https://github.com/vueComponent/ant-design-vue) - Ant Design Of Vue 实现
- [@antv/g2](https://antv.alipay.com/zh-cn/index.html) - Alipay AntV 数据可视化图表
- [Viser-vue](https://viserjs.github.io/docs.html#/viser/guide/installation) - antv/g2 封装实现

## 项目下载和运行

- 安装依赖

```bash
yarn install
```

- 开发模式运行

```bash
yarn run serve
```

- 编译项目

```bash
yarn run build
```

- Lints and fixes files

```bash
yarn run lint
```

## 目录结构

```bash
src
├── App.vue     # 主文件
├── api         # Mock 接口文件
├── assets      # 资源文件
├── components  # 自定义组件
├── config      # 配置
├── layouts     # 布局
├── main.js     # 主文件
├── model       # 数据请求模型
├── pages       # 具体页面
├── router      # 路由配置
├── store       # vuex 状态
└── utils       # 工具库
```

## Mock

Use mockjs, mock 文件存放目录 `./src/api`, 支持 `.js`,`.json`.

```javascript
/**
 * @url /order/add
 *
 */
module.exports = function(req) {
  return {
    success: Math.random() < 0.5 ? false : true,
    msg: '@word',
    code: Math.random() < 0.5 ? -200 : 0,
  };
};
```

or

```json
/**
 * @url /order/add
 *
 */
{
  "msg": "@word",
  "code": 200
}
```

## 提交规范

Commit message 的格式

```bash
<type>(<scope>): <subject>
# 空一行
<body>
# 空一行
<footer>
```

常用的 type 类别

- feat：新功能（feature）
- fix：修补 bug
- docs：文档（documentation）
- style： 格式（不影响代码运行的变动）
- refactor：重构（即不是新增功能，也不是修改 bug 的代码变动）
- test：增加测试
- chore：构建过程或辅助工具的变动

```bash
# 例子
git commit -m 'feat: 增加 xxx 功能'
git commit -m 'bug: 修复 xxx 功能'
```
