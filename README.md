# blackmatrix7-surge-mirror

blackmatrix7/ios_rule_script 中 `rule/Surge` 被实际引用的 16 个规则集镜像。每日自动同步（上游有变更才提交）。

## 上游删库时切换 Surge 配置

Rule.dconf 中把

```
https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/
```

全部替换为

```
https://raw.githubusercontent.com/mickeu/blackmatrix7-surge-mirror/main/
```

路径其余部分完全一致（如 `rule/Surge/ChinaMax/ChinaMax_All.list`），共 16 处。

## 覆盖范围（与 Rule.dconf 引用一一对应）

Advertising_All / ChinaMax_All / Global_All / GlobalMedia_All / Global / ChinaMedia / Lan /
OpenAI / Claude / Microsoft / Game / YouTube / Netflix / Disney / Spotify / TikTok / BiliBili

## 同步方式

本机 minis-scheduled 每日 11:30 运行 `blackmatrix7-mirror-sync.py`（GitHub Contents API，幂等）。
