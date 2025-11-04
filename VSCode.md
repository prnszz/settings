{
  "typescript.suggest.paths": false,
  "javascript.suggest.paths": false,
  "files.associations": {
    "*.jsx": "javascriptreact",
    "*.tsx": "typescriptreact"
  },

  // Git 
  "git.enableSmartCommit": true,
  "git.autofetch": true,
  "git.confirmSync": false,

  // Emmet 
  "emmet.triggerExpansionOnTab": true,
  "emmet.showAbbreviationSuggestions": true,
  "emmet.showExpandedAbbreviation": "always",
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "typescript": "typescriptreact"
  },

  "editor.fontSize": 14,
  "editor.wordWrap": "on",
  "editor.detectIndentation": false,
  "editor.tabSize": 2,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.decorations.colors": false,

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
    // "source.organizeImports": "explicit"
  },
  "workbench.iconTheme": "vscode-icons",

  "editor.minimap.enabled": false,
  "editor.renderWhitespace": "none",

  // "restoreTerminals.runOnStartup": true,
  // "restoreTerminals.terminals": [
  //   {
  //     "splitTerminals": [
  //       {
  //         "name": "Terminal",
  //         "commands": ["y"]
  //       }
  //     ]
  //   }
  // ],
  "editor.fontFamily": "Hack Nerd Font Mono, 'Microsoft YaHei', 'PingFang SC', 'Hiragino Sans', 'Noto Sans CJK SC', 'Noto Sans CJK JP', monospace",
  "workbench.colorTheme": "Atom One Light",
  "[markdown]": {
    "diffEditor.ignoreTrimWhitespace": false
  },
  "github.copilot.enable": {
    "*": true,
    "plaintext": false,
    "markdown": true,
    "scminput": false
  },
  "extensions.ignoreRecommendations": true,
  "window.autoDetectColorScheme": true,
  "workbench.preferredLightColorTheme": "Atom One Light",
  "workbench.preferredDarkColorTheme": "Atom One Dark",
  "python.createEnvironment.trigger": "off",
  "githubPullRequests.fileListLayout": "flat",
  "githubPullRequests.pullBranch": "never",
  "diffEditor.codeLens": true,
  "github.copilot.nextEditSuggestions.enabled": true,
  "workbench.editor.empty.hint": "hidden",
  }
