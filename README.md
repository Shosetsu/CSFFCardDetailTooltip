# 卡牌详情数据显示 - 《卡牌生存：奇幻森林》Mod

[![zh](https://img.shields.io/badge/lang-zh-red.svg)](https://github.com/Shosetsu/CSFFCardDetailTooltip/blob/master/README.md)
[![en](https://img.shields.io/badge/lang-en-blue.svg)](https://github.com/Shosetsu/CSFFCardDetailTooltip/blob/master/README_en.md)

本 Mod 在鼠标悬停时于提示框（tooltip）中显示卡牌的状态与进度相关详细信息。

[预览图](pic/screenshot1.png)

# 使用方法

## 安装 BepInEx

本 Mod 作为 BepInEx 5 框架的插件运行。

安装指南请参见：<https://docs.bepinex.dev/v5.4.21/articles/user_guide/installation/index.html>

## Mod 安装

- 从发布页下载最新版本：<https://github.com/Shosetsu/CSFFCardDetailTooltip/releases>
- 将 `CSFFDetailedCardProgress.dll` 解压至游戏目录下的 `BepInEx/plugins` 文件夹中。

## 设置（可选）

配置文件位于：`/BepInEx/config/CSFFCardDetailTooltip.cfg`

| 名称                          | 默认值   | 说明                                                |
| ----------------------------- | -------- | --------------------------------------------------- |
| Enabled                       | true     | 启用后将显示详细提示信息                            |
| HotKey                        | F2       | 切换提示信息显示状态的快捷键                        |
| RecipesShowTargetDuration     | false    | 若为 true，陷阱等制作装置将显示精确处理时间而非范围 |
| HideImpossibleDropSet         | true     | 若为 true，将隐藏不可能掉落的物品组合               |
| TooltipNextPageHotKey         | 右方括号 | 显示提示下一页的快捷键                              |
| TooltipPreviousPageHotKey     | 左方括号 | 显示提示上一页的快捷键                              |
| AdditionalEncounterLogMessage | false    | 若为 true，战斗遭遇事件的消息日志中将显示额外提示   |
| ForceInspectStatInfos         | false    | 若为 true，强制使“细菌热”等状态可被检查             |

**切换提示说明**：使用快捷键启用或禁用详细提示后，当前悬停的卡牌提示不会立即更新，需移开鼠标后再重新悬停才会生效。

# 已知问题

- 尚未完全适配 CSFF 的新战斗系统。
- 可能存在部分文字排版或拼写问题。

# 更新日志

## 1.0.0

- 适配《卡牌生存：奇幻森林》（CSFF）。

## 1.0.1

- 修正钓鱼事件的概率显示错误。

## 1.0.2

- 新增对 CSFF 陷阱系统重做后的兼容支持。

## 1.0.3 ~ 1.0.5

- 优化 Stat 处理逻辑，显著提升游戏性能（尤其在后期）。

## 1.0.6

- 修复 Encounter.cs 中的类型定义错误。

## 1.0.7

- 修复液体容器详情中 SpoilageRateModifier 未正确处理的问题。

## 1.0.8

- 删除未支持的 WeatherCardInspectable 相关处理。
- 删除背包按钮显示负重的相关处理，请使用[WikiMod](https://csff-db.uuppi.com/_WikiMod) 1.0.6 版本或更高版本代替。
