初始化
添加 husky commitlint
## git不支持中文
git commit 代码时提示:Warning: Your console font probably doesn‘t support Unicode. If you experience trange characters in the output, consider switching to a TrueType font such as ucida Console!
idea git commit 不支持中文 -m .

依次执行以下命令：中括号里可选

git config [--global] core.quotepath off
git config [--global] --unset i18n.logoutputencoding
git config [--global] --unset i18n.commitencoding
再次git commit就OK了，可以中文了。
