从该站学习[ModDota](https://moddota.com/)

### 0. VSCode中的插件推荐

- dota-reborn-code (Dota KV文件提示,lua提示等): https://marketplace.visualstudio.com/items?itemName=XavierCHN.dota-reborn-code
- dota2-作图工具 (查询API,一些API有中文注释,也有代码提示,但没有上面的那个好用,我用它来查询API和其他东西): https://marketplace.visualstudio.com/items?itemName=bigciba.dota2-tools
- Dota2 Coding Helper (api查询等,客户端api查询在我电脑上挂了,其他功能暂未体验,他也是[Dota2 Simple GUI](https://marketplace.visualstudio.com/items?itemName=robincode.dota2-simple-gui)的作者,不过github上说迁移了): https://marketplace.visualstudio.com/items?itemName=robincode.dota2-coding-helper


### 1.地图编辑器操作: https://developer.valvesoftware.com/wiki/Dota_2_Workshop_Tools:zh-cn/Level_Design:zh-cn/Tile_Editor_Basics:zh-cn

### 2. [Script](https://moddota.com/scripting-introduction/)
  
  - 解包其他mod和如何在Github搜索代码: https://moddota.com/scripting-introduction/#scripting-examples-and-sources
  - API站点: https://developer.valvesoftware.com/wiki/Dota_2_Workshop_Tools/Scripting/API
  - 内置事件: https://developer.valvesoftware.com/wiki/Dota_2_Workshop_Tools/Scripting/Built-In_Engine_Events
  

### 3.[TypeScript To Lua](https://moddota.com/scripting/Typescript/typescript-introduction)
  
  - TypeScript Addon Template ([使用](https://moddota.com/scripting/Typescript/typescript-introduction#setting-up-typescript)): https://github.com/ModDota/TypeScriptAddonTemplate
  - TypeScript 模板中的一些说明: https://moddota.com/scripting/Typescript/typescript-introduction#typescript-addon-structure
  - TypeScript 模板更新(挺慢的): https://moddota.com/scripting/Typescript/typescript-introduction#updating-your-addon
  - TypeScript 模板自动检测变更并翻译: https://moddota.com/scripting/Typescript/typescript-introduction/#activating-the-watcher
  - TypeScript 模板tsconfig.json设置类型: https://moddota.com/scripting/Typescript/typescript-introduction/#normalized-types
  - TypeScript 模板例子: https://moddota.com/scripting/Typescript/typescript-introduction/#integrated-examples
  - 多语言: https://moddota.com/scripting/Typescript/tooltip-generator/
  - - [启动和关闭语言项](https://moddota.com/scripting/Typescript/tooltip-generator/#language-control),在resource目录下的language.ts中注释和取消注释枚举即可,该操作需要重新开启一下Watch(ctrl+shift+b)或者`npm run dev`
  - - [教程作者的一个文件家规范方式](https://github.com/Shushishtok/dota-reimagined/tree/master/game/resource/localization)

### 4. 技能图标

  - 内置图标名: https://developer.valvesoftware.com/wiki/Dota_2_Workshop_Tools/Scripting/Built-In_Ability_Names

## Other

- 使用`SetCustomHeroMaxLevel`API可以设置英雄最大等级,在TypeScript中为`GameRules.GetGameModeEntity().SetCustomHeroMaxLevel(100);`
