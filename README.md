<h1  align="center">
	<img    alt="Vscode"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590162763/vscode-plugins/angular-ts-code1_gkgjjn.png">
	<br/>
	Configuração de Plugins para o Vscode e Inicialização do Eslint para Projetos Angular
</h1>

# 😱 Desafio Proposto

> Melhorar o experiência de desenvolvimento da equipa utilizando um lint para padronizar o código fonte da aplicação. Aceitei o desafio e aqui estou criando esse documento para mostrar todos os passos realizados até alcançar o objetivo.

<h3  >
	1º Passo: Vamos iniciar instalando alguns plugins e configurar o VSCode.
</h3>
<br>

# ❤️ Instalando Plugins

- **EditorConfig for VS Code**

<img    alt="EditorConfig"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590163234/vscode-plugins/Editor_config_qwql0j.gif">

- **Prettier - Code formatter**

<img    alt="Prettier"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590163489/vscode-plugins/prettier_jsw4z1.gif">

- **Material Icon Theme**

<img    alt="Material"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590163656/vscode-plugins/Material_hqv522.gif">

- **ESLint**

<img    alt="ESLint"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590164210/vscode-plugins/eslint_q9cvw8.gif">

- **Dracula Official**

<img    alt="Dracula"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590164208/vscode-plugins/Dracula_ncqsi8.gif">

- **GitLens — Git supercharged**

<img    alt="GitLens"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590164212/vscode-plugins/gitlens_k1vxz3.gif">

# 🔥 Configurando settings.json

```json
{
  "workbench.startupEditor": "newUntitledFile",
  "terminal.integrated.fontSize": 14,
  "editor.tabSize": 2,
  "editor.fontSize": 14,
  "editor.lineHeight": 24,
  "editor.fontFamily": "Fira Code",
  "editor.fontLigatures": true,
  "explorer.compactFolders": false,
  "editor.renderLineHighlight": "gutter",
  "workbench.editor.labelFormat": "short",
  "extensions.ignoreRecommendations": true,
  "javascript.updateImportsOnFileMove.enabled": "never",
  "typescript.updateImportsOnFileMove.enabled": "never",
  "breadcrumbs.enabled": true,
  "editor.parameterHints.enabled": false,
  "explorer.confirmDragAndDrop": false,
  "explorer.confirmDelete": false,
  "editor.rulers": [80, 120],
  "editor.formatOnSave": true,
  "enableTelemetry": true,
  "emmet.syntaxProfiles": {
    "javascript": "jsx"
  },
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  },
  "[javascript]": {
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    }
  },
  "[javascriptreact]": {
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    }
  },
  "[typescript]": {
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    }
  },
  "[typescriptreact]": {
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    }
  },
  "workbench.colorTheme": "Dracula"
}
```

<h3  >
	2º Passo: Configurar o EditorConfig.
</h3>
<br>

# 🤓 Configurando EditorConfig

- **Generate EditorConfig**

<img    alt="Generate EditorConfig"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590167481/vscode-plugins/generateEditorConfig_mpvv5t.gif">

- **Configurando .editorconfig**

```javascript
root = true

[*]
end_of_lines=lf
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```

# 🤓 Configurando ESlint

- **Instalação**

```sh
npm i --save-dev eslint
```

- **Iniciando Configurações**

```sh
./node_modules/.bin/eslint --init
```

<img  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600748/vscode-plugins/1_kgzhdf.png">

<br/>

<img  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600748/vscode-plugins/3_juab6r.png">

<br/>

<img  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600748/vscode-plugins/3_juab6r.png">

<br/>

<img   src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600749/vscode-plugins/4_eea5oo.png">

<br/>

<img   src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600749/vscode-plugins/5_v97ow0.png">

<br/>

<img   src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600748/vscode-plugins/6_rfgecm.png">

<br/>

<img   src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600750/vscode-plugins/7_i6xpiy.png">

<br/>

<img   src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600749/vscode-plugins/8_skfd11.png">

<br/>

<img   src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600749/vscode-plugins/9_wfqir8.png">

<br/>

<img   src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590600749/vscode-plugins/10_anexw6.png">

- **Intalando Dependências Prittier**

```sh
npm i --save-dev eslint eslint-config-prettier eslint-plugin-prettier eslint-import-resolver-typescript
```

- **eslinrc.json**

```json
{
  "env": {
    "browser": true,
    "es6": true
  },
  "extends": [
    "airbnb-base",
    "plugin:@typescript-eslint/eslint-recommended",
    "prettier/@typescript-eslint",
    "plugin:prettier/recommended",
    "plugin:@typescript-eslint/recommended"
  ],
  "globals": {
    "Atomics": "readonly",
    "SharedArrayBuffer": "readonly"
  },
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": 11,
    "sourceType": "module"
  },
  "plugins": ["@typescript-eslint", "prettier"],
  "rules": {
    "@typescript-eslint/explicit-module-boundary-types": "off",
    "prettier/prettier": ["error", { "singleQuote": true, "parser": "flow" }],
    "class-methods-use-this": "off",
    "@typescript-eslint/camelcase": "off",
    "no-useless-constructor": "off",
    "@typescript-eslint/no-unused-vars": [
      "error",
      { "argsIgnorePattern": "_" }
    ],
    "@typescript-eslint/interface-name-prefix": [
      "error",
      { "prefixWithI": "always" }
    ],
    "import/extensions": [
      "error",
      "ignorePackages",
      {
        "ts": "never"
      }
    ]
  },
  "settings": {
    "import/resolver": {
      "typescript": {}
    }
  }
}
```

- **eslinignore.json**

```json

 /*.js
  node_modules
  dist
  assembly
  e2e

```

- **prettier.config.js**

```javascript
module.exports = {
  singleQuote: true,
  trailingComma: "all",
  arrowParens: "avoid",
};
```
