# Sublime Text Plugins

# Package Control

安装所有 SublimeText 插件的前提

# Emmet

中文文档：[地址][1]
[前端开发必备！Emmet使用手册][2]

# Alignment

# BracketHighlighter

# DocBlockr

可以快速的对函数进行注释。保存代码规范
支持多种语言。（个人觉得brackets的这个插件比Sublime Text做得好多了。）

`/*` : 回车创建一个代码块注释
`/**` : 回车在自动查找函数中的形参等等。

它会生成 JSDoc 格式的注释。如果你从没有使用过类似的工具，DocBlockr 会让你觉得以前没有它是如何写代码的。帮助你创造你的代码注释，通过解析功能，参数，变量，并且自动添加基本项目。

# Git & GitGutter

可视化的操作：帮助你与你的Git repo协议进行交互。它支持很多命令像init, push, pull, branch, stash,等等。了解更多关于你在Sublime Text里面究竟能使用哪些Git功能，以提高您的工作流程。
[使用参考][3]

`GitGutter`:
Sublime Text 有了 Git 插件之后，GitGutter 更好的帮助开发者查看文件之前的改动和差异，提升开发效率。

# JsFormat

刚开始在JSX文件格式化后惨不忍睹，其实配置一个属性就可以支持JSX语法格式化。
`菜单->Preferences->Package Settings->JsFormat->Settings-User`加入以下代码

    {
      "e4x": true,//支持jsx格式化
      "format_on_save": true//保存立即格式化，看个人喜好
    }

# Babel

Sublime3才有的插件，支持ES6、JSX语法高亮。

# ConvertToUTF8


# SublimeCodeIntel

# ColorPicker

# ESLint

# Color Highlighter

前端编辑颜色时，这个插件会显示相应颜色代码的实际颜色。

## ReactJS Snippets
React语法高亮、代码提示...

        cdm→  componentDidMount: fn() { ... }
       cdup→  componentDidUpdate: fn(pp, ps) { ... }
         cs→  var cx = React.addons.classSet;
        cwm→  componentWillMount: fn() { ... }
        cwr→  componentWillReceiveProps: fn(np) { ... }
        cwu→  componentWillUpdate: fn(np, ns) { ... }
       cwun→  componentWillUnmount: fn() { ... }
         cx→  cx({ ... })
        fdn→  React.findDOMNode(...)
        fup→  forceUpdate(...)
        gdp→  getDefaultProps: fn() { return {...} }
        gis→  getInitialState: fn() { return {...} } 
        ism→  isMounted()
      props→  this.props.
         pt→  propTypes { ... }
        rcc→  component skeleton
       refs→  this.refs.
        ren→  render: fn() { return ... }
        scu→  shouldComponentUpdate: fn(np, ns) { ... }
        sst→  this.setState({ ... })
      state→  this.state.

## React ES6 Snippets
ES6 Snippets，代码提示

  [1]: http://yanxyz.github.io/emmet-docs/css-abbreviations/vendor-prefixes/
  [2]: http://www.w3cplus.com/tools/emmet-cheat-sheet.html
  [3]: https://scotch.io/tutorials/using-git-inside-of-sublime-text-to-improve-workflow