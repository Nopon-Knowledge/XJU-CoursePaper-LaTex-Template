# 课程论文模板使用教程

本项目为西京学院课程论文的LaTex模板，旨在帮助你更好更快地完成课程论文。

须使用xelatex编辑器，如果你用的是overleaf，进设置compiler部分选择xelatex即可。

如果用的是vscode中的latex workshop插件，则需要在项目中新建.vscode文件夹，再新建setting.json文件。将以下代码复制进去，再进行编译即可。

```
{
  // 禁止它自动乱选（可选，但很推荐）
  "latex-workshop.latex.autoBuild.run": "never",

  // 关键：默认 recipe 设为 latexmk(xelatex)
  "latex-workshop.latex.recipe.default": "latexmk (xelatex)",

  "latex-workshop.latex.recipes": [
    { "name": "latexmk (xelatex)", "tools": ["latexmk-xelatex"] }
  ],

  "latex-workshop.latex.tools": [
    {
      "name": "latexmk-xelatex",
      "command": "latexmk",
      "args": [
        "-xelatex",
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "-outdir=%OUTDIR%",
        "%DOC%"
      ]
    }
  ]
}

```