# 意大利行程 2026/10/01–10/13

一个静态网页，没有任何后端和依赖，打开 `index.html` 就能看。

## 怎么改内容

所有行程数据都在 `index.html` 里的 `<script>` 段，格式很直观：

- `HOTELS` —— 四家酒店
- `DAYS` —— 逐日行程，每天一个 `{ d:'日期', city:'城市', items:[...] }`
- 每个 `items` 里的项目：
  - `t` 开始时间 / `e` 结束时间
  - `n` 标题
  - `k` 类型：fly 航班 · train 火车 · bus 车 · boat 船 · see 景点 · eat 吃饭 · stay 住宿 · meet 集合 · walk 步行
  - `b:1` 表示已预订（绿框）
  - `warnFlag:1` 表示要留意（黄框）
  - `m` 地图按钮 `[['显示的名字','Google 地图搜索词']]`
  - `r` 明细行 `[['标签','内容']]`
  - `warn` 注意事项 · `bring` 携带物品 · `tip` 小提示 · `note` 说明

改完保存、提交，GitHub Pages 一两分钟后自动更新。

## GitHub Pages

Settings → Pages → Source 选 `main` 分支 `/ (root)`，保存即可。
