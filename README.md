FIS Components 规范说明
====

此规范大部分借鉴了[component](https://github.com/componentjs/component)的思想。

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
