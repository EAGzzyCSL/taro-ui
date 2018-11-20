# 常见问题

本章节收集了网友常问问题，提问之前请先阅读该章节

## 出现xx问题怎么办

在提问时，请确保 taro-ui 已经是最新版本了，并确保 taro 版本在 1.0.7 以上

## 如何自定义样式

审查元素的样式，进行覆盖，考虑到样式优先级问题，可用 `!important` 增加优先级，或增加 `className`，然后使用比如`.myClass.at-tabs` 这样的方式增加优先级。

## 自定义样式为什么没有生效（h5 生效，小程序没生效）

taro-ui 自定义样式覆盖小程序组件样式使用到了 globalClass 这个小程序特性，由于小程序的限制，自定义的样式需要在 page 页面内使用，不能基于第三方组件再进行一层封装，这样做样式会无效。并且确保小程序调试基础库在 2.2.3 以上

## 如何修改边框、下划线样式

边框下划线有些组件是使用 `::after` 伪类，在微信开发者工具审查不到，但是实际是存在的，建议用 H5 模式审查样式。