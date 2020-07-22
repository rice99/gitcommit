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

### 上面的解决方案无效，需要使用下面的
git config --global core.quotepath false
git config --global gui.encoding utf-8
git config --global i18n.commit.encoding utf-8
git config --global i18n.logoutputencoding utf-8
set LESSCHARSET=utf-8
这样设置完后，当前命令窗口是没问题的。但是，另打开一个还是不行。然后就想到应该是最后一句的问题。这一个并没有将这个变量保存起来。所以，就直接将最后一个变量添加到Windows环境变量中