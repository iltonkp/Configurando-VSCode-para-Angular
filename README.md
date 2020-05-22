<h1  align="center">
	<img    alt="Vscode"  width="500" height="200"  src="https://res.cloudinary.com/dpeywfgot/image/upload/v1590162763/vscode-plugins/angular-ts-code1_gkgjjn.png">
	<br/>
	Configuração de Plugins para o Vscode e Inicialização do Eslint para Projetos Angular
</h1>

# Instalando Plugins

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

# Configurando settings.json

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
