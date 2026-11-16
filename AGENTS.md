# 仓库约定

## 远程仓库

- `origin` 是本仓库的 fork: `git@github.com:zhufengning/qbob.git`, 日常提交推送到这里
- `upstream` 是上游: `https://github.com/Loping151/qbob.git`, 只用于拉取更新, 不向上游推送

拉取并合并上游:

```bash
git fetch upstream
git merge upstream/main
```

合并前先提交本地更改. 冲突处同时保留上游改动与本仓库改动; 合并后确认 `qqbot_onebot` 可以正常编译.

## 更新日志

`CHANGELOG.md` 顶部的 `## Fork 更改` 记录本仓库相对上游的更改. 上游自己的发布记录保持在下面, 不改写.

- 每条更改以 `YYYY-MM-DD` 开头, 日期取更改完成的日期
- 新更改追加在本节末尾, 同一天的多条更改按修改顺序排列
- 标题不使用 `## 未发布`
- 条目写最终行为, 不写被否决的思路, 也不写修改前后的对比

## 提交

按主题分批提交, 一次提交只包含一类更改. 同步上游产生的合并提交与功能更改分开提交.
