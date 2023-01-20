# FAQ

- 如何检查自己输入的条件在软件中是怎么产生影响的？

  推荐使用方程视图。

- 当已知区域、面或者边的代号的时候，怎么快速选择？

  在选择框右侧两竖列图标中，有一个***粘贴选择*** 图标。一般情况下这个功能是用来粘贴被复制的选择，但是也可以直接键入选择。此时直接键入已知的代号即可。

- How to open the “equation view”?

- How to simulated metallized models?

  在选择物理场借口时，应按照以下方式。

  1. 弱形式偏微分方程(w)：场名称 `u`，因变量数 `3`，因变量 `u`、`v`、`w`，因变量单位 `m`。
  2. 弱形式偏微分方程(w2)：场名称 `EM`，因变量数 `3`，因变量 `Mx`、`My`、`Mz`，因变量单位 `V/m / (rad/s)`。

  电磁场的参数定义应该改成：

  [全局变量 - 电磁场（不考虑环境时） (1)](https://www.notion.so/1-59b70e6008a34ecaa00b49805e7b19ce)