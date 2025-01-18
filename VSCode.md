# User settings
```
{
  "typescript.suggest.paths": false,
  "javascript.suggest.paths": false,
  // 文件类型关联配置，告诉 VS Code 如何解析特定文件扩展名
  "files.associations": {
    // 将 .jsx 文件识别为 React JavaScript 文件
    "*.jsx": "javascriptreact",
    // 将 .tsx 文件识别为 React TypeScript 文件
    "*.tsx": "typescriptreact"
  },

  // Git 相关配置
  // 启用智能提交功能，当暂存区为空时，会自动将所有更改的文件加入提交
  "git.enableSmartCommit": true,
  // 自动从远程仓库获取更新
  "git.autofetch": true,
  // 执行同步操作时不显示确认对话框
  "git.confirmSync": false,

  // Emmet 配置（用于快速编写 HTML/CSS 的工具）
  // 按 Tab 键时触发 Emmet 展开缩写
  "emmet.triggerExpansionOnTab": true,
  // 显示 Emmet 缩写建议
  "emmet.showAbbreviationSuggestions": true,
  // 始终显示展开的 Emmet 缩写预览
  "emmet.showExpandedAbbreviation": "always",
  // 在 JavaScript 和 TypeScript 文件中启用 Emmet
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "typescript": "typescriptreact"
  },

  // 编辑器基本设置
  // 设置字体大小为 14px
  "editor.fontSize": 14,
  // 启用自动换行
  "editor.wordWrap": "on",
  // 禁用自动检测缩进
  "editor.detectIndentation": false,
  // 设置缩进大小为 2 个空格
  "editor.tabSize": 2,
  // 设置默认的代码格式化工具为 Prettier
  "editor.defaultFormatter": "esbenp.prettier-vscode",

  // 特定语言的格式化设置
  // JavaScript 文件的专门配置
  "[javascript]": {
    // 保存时自动格式化
    "editor.formatOnSave": true,
    // 使用 Prettier 作为格式化工具
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  // TypeScript 文件的专门配置
  "[typescript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  // JSX 文件的专门配置
  "[javascriptreact]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  // TSX 文件的专门配置
  "[typescriptreact]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },

  // 窗口设置
  // 设置窗口的缩放级别
  "window.zoomLevel": 1,

  // 文件自动保存设置
  // 当编辑器失去焦点时自动保存文件
  "files.autoSave": "onFocusChange",

  // 搜索排除配置：这些文件夹在搜索时会被忽略
  "search.exclude": {
    // 排除 node_modules 文件夹
    "**/node_modules": true,
    // 排除 Next.js 构建输出目录
    "**/.next": true,
    // 排除其他常见的构建输出目录
    "**/out": true,
    "**/build": true,
    "**/dist": true,
    "**/git": true
  },

  // 文件排除配置：这些文件/文件夹在 VS Code 的文件浏览器中不会显示
  "files.exclude": {
    // 隐藏版本控制系统的文件夹
    "**/.git": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/CVS": true,
    // 隐藏 macOS 系统文件
    "**/.DS_Store": true,
    // 隐藏 node_modules 文件夹
    "**/node_modules": true,
    // 隐藏 Next.js 构建输出目录
    "**/.next": true
  },

  // Prettier 格式化工具的配置
  // 在语句末尾添加分号
  "prettier.semi": true,
  // 使用单引号而不是双引号
  "prettier.singleQuote": true,
  // 配置尾随逗号的方式
  "prettier.trailingComma": "es5",
  // 设置每行缩进的空格数
  "prettier.tabWidth": 2,
  // 设置每行代码的最大长度
  "prettier.printWidth": 100,

  // TypeScript 相关配置
  // 移动/重命名文件时自动更新导入语句
  "typescript.updateImportsOnFileMove.enabled": "always",
  // 启用自动导入建议
  "typescript.suggest.autoImports": true,

  // 保存时的自动操作配置
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit",
    "source.organizeImports": "explicit"
  },
  "workbench.iconTheme": "vscode-icons",

  "vim.leader": "<Space>",
  "vim.hlsearch": true,
  "vim.insertModeKeyBindings": [
    {
      "before": ["j", "k"],
      "after": ["<Esc>"]
    }
  ],
  "vim.normalModeKeyBindingsNonRecursive": [
    // NAVIGATION
    // 5 lines movement
    { "before": ["J"], "after": ["5", "j"] },
    { "before": ["K"], "after": ["5", "k"] },

    { "before": ["H"], "after": ["^"] },
    { "before": ["L"], "after": ["$"] },
    // { "before": ["<S-h>"], "commands": [":bprevious"] },
    // { "before": ["<S-l>"], "commands": [":bnext"] },

    // splits
    { "before": ["leader", "v"], "commands": [":vsplit"] },
    // { "before": ["leader", "s"], "commands": [":split"] },
    { "before": ["leader", "s"], "commands": ["editor.action.commentLine"] },

    // panes
    { "before": ["leader", "d"], "after": ["o", "<Esc>"] },
    { "before": ["leader", "a"], "commands": ["editor.action.indentLines"] },
    { "before": ["leader", "f"], "commands": ["editor.action.outdentLines"] },
    {
      "before": ["leader", "h"],
      "commands": ["workbench.action.focusLeftGroup"]
    },
    // {
    //   "before": ["leader", "j"],
    //   "commands": ["workbench.action.focusBelowGroup"]
    // },
    // {
    //   "before": ["leader", "k"],
    //   "commands": ["workbench.action.focusAboveGroup"]
    // },
    {
      "before": ["leader", "l"],
      "commands": ["workbench.action.focusRightGroup"]
    },
    // NICE TO HAVE
    // { "before": ["leader", "w"], "commands": [":w!"] },
    // { "before": ["leader", "q"], "commands": [":q!"] },
    // { "before": ["leader", "x"], "commands": [":x!"] },
    {
      "before": ["[", "d"],
      "commands": ["editor.action.marker.prev"]
    },
    {
      "before": ["]", "d"],
      "commands": ["editor.action.marker.next"]
    },
    {
      "before": ["<leader>", "c", "a"],
      "commands": ["editor.action.quickFix"]
    },
    // { "before": ["leader", "f"], "commands": ["workbench.action.quickOpen"] },
    { "before": ["leader", "p"], "commands": ["editor.action.formatDocument"] },
    {
      "before": ["g", "h"],
      "commands": ["editor.action.showDefinitionPreviewHover"]
    }
  ],
  "vim.visualModeKeyBindings": [
    // Stay in visual mode while indenting
    { "before": ["<"], "commands": ["editor.action.outdentLines"] },
    { "before": [">"], "commands": ["editor.action.indentLines"] },
    // Move selected lines while staying in visual mode
    { "before": ["J"], "commands": ["editor.action.moveLinesDownAction"] },
    { "before": ["K"], "commands": ["editor.action.moveLinesUpAction"] },
    // toggle comment selection
    { "before": ["leader", "c"], "commands": ["editor.action.commentLine"] }
  ],
  "vim.autoSwitchInputMethod.enable": true,
  "vim.autoSwitchInputMethod.defaultIM": "com.apple.keylayout.ABC",
  "vim.autoSwitchInputMethod.obtainIMCmd": "/opt/homebrew/bin/im-select",
  "vim.autoSwitchInputMethod.switchIMCmd": "/opt/homebrew/bin/im-select {im}",
  "editor.minimap.enabled": false,
  "editor.renderWhitespace": "all",

  "restoreTerminals.runOnStartup": true,
  "restoreTerminals.terminals": [
    {
      "splitTerminals": [
        {
          "name": "Terminal",
          "commands": ["y"]
        }
      ]
    }
  ],
  "editor.fontFamily": "Hack Nerd Font Mono",
  "workbench.colorTheme": "Atom One Light",
  "[markdown]": {
    "diffEditor.ignoreTrimWhitespace": false
  },
  "github.copilot.enable": {
    "markdown": true
  }
}
```

# keybindings.json
```
[
  // NAVIGATION
  {
    "key": "ctrl+shift+a",
    "command": "workbench.action.terminal.focusNext",
    "when": "terminalFocus"
  },
  {
    "key": "ctrl+shift+b",
    "command": "workbench.action.terminal.focusPrevious",
    "when": "terminalFocus"
  },
  {
    "key": "ctrl+shift+j",
    "command": "workbench.action.togglePanel"
  },
  {
    "key": "ctrl+shift+n",
    "command": "workbench.action.terminal.new",
    "when": "terminalFocus"
  },
  {
    "key": "ctrl+shift+w",
    "command": "workbench.action.terminal.kill",
    "when": "terminalFocus"
  },
  // FILE TREE
  {
    "command": "workbench.action.toggleSidebarVisibility",
    "key": "ctrl+e"
  },
  {
    "command": "workbench.files.action.focusFilesExplorer",
    "key": "ctrl+e",
    "when": "editorTextFocus"
  },
  // {
  //   "command": "worokench.action.toggleSidebarVisibility",
  //   "key": "ctrl+f",
  // },
  {
    "command": "workbench.action.findInFiles",
    "key": "ctrl+f",
    "when": "editorTextFocus"
  },
  {
    "key": "n",
    "command": "explorer.newFile",
    "when": "filesExplorerFocus && !inputFocus"
  },
  {
    "command": "renameFile",
    "key": "r",
    "when": "filesExplorerFocus && !inputFocus"
  },
  {
    "key": "shift+n",
    "command": "explorer.newFolder",
    "when": "explorerViewletFocus"
  },
  // {
  //   "key": "shift+n",
  //   "command": "workbench.action.newWindow",
  //   "when": "!explorerViewletFocus"
  // },
  {
    "command": "deleteFile",
    "key": "d",
    "when": "filesExplorerFocus && !inputFocus"
  },

  // EXTRA
  {
    "key": "shift+cmd+\\",
    "command": "workbench.action.createTerminalEditor"
  },
  {
    "key": "cmd+e",
    "command": "-actions.findWithSelection"
  },
  {
    "key": "cmd+e",
    "command": "-editor.action.toggleScreenReaderAccessibilityMode",
    "when": "accessibilityHelpIsShown"
  },
  {
    "key": "cmd+b",
    "command": "-markdown.extension.editing.toggleBold",
    "when": "editorTextFocus && !editorReadonly && editorLangId =~ /^markdown$|^rmd$|^quarto$/"
  },
  {
    "key": "ctrl+;",
    "command": "extension.aceJump",
  },
  {
    "key": "ctrl+'",
    "command": "extension.aceJump.multiChar",
  },
  {
    "key": "ctrl+[", 
    "command": "extension.aceJump.line",
  },
  {
    "key": "ctrl+g",
    "command": "-extension.vim_ctrl+g",
    "when": "editorTextFocus && vim.active && vim.use<C-g> && !inDebugRepl"
  },
 ]
