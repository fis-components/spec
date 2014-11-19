FIS 模块规范说明
====

此规范借鉴了很多[component](https://github.com/componentjs/component)的思想。

一个模块可以由 HTML/TPL、JS、CSS、Images、Fonts和其他前端资源的任意组合组成，它应该具有一定的通用性和独立性。每个模块必须包含 [components.json](#componentjson) 文件来描述自己。一个模块可以通过指定依赖，使用其他模块。

如果模块中包含 JS，JS 应该采用 COMMONJS 规范或者 AMD 规范来解决依赖和对外暴露的问题。模块对于其依赖的引用，请通过模块名来指定，如 `require('jquery')`。

## component.json
每个组件必须包含一个 `component.json` 文件来描述此组件信息。

```json
{
  "name": "dialog",
  "description": "一个简单的 dialog 组件",
  "dependencies": [
    "github://xiangshouding/glob.js@master",
    "gitlab://fis-dev/fis-report-record@master",
    "lights://pc-demo@latest"
  ],
  "roadmap":[
    {
      "reg": "**.css",
      "release": "styles/$&"
    },
    
    {
      "reg": "*",
      "release": false
    }
  ]
}
```
