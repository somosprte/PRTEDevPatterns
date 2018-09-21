# Editor

1. [VS Code](#vs-code)
2. [Extensões](#extensões)
3. [Configurações](#configurações)
4. [Teclas de Atalho](#teclas-de-atalho)
5. [Snippets](#snippets)


## VS Code

![VS Code](https://code.visualstudio.com/assets/home/home-screenshot-mac-lg-2x.png)

O VS Code tem se mostrado uma excelente IDE para desenvolvimento. Completa e muito leve, tornando o
desenvolvimento muito mais produtivo.

[Faça o Download](https://code.visualstudio.com/)

### Extensões 

- **Auto Close Tag**: Adiciona automaticamente as tags de fechamento do HTML/XML.
- **Color Hightlight**: Adiciona um destaque nas chamadas de cores.
- **Dracula Official**: Tema de cores para o VS Code.
- **EditorConfig for VS Code**: Essa extensão da suporte ao VS Code para interpretar o arquivo _.editorconfig_, que define
  os padrões de desenvolvimento do projeto.
- **ESLint**: Essa extensão da suporte ao VS Code para interpretar os padrões definidos pelo _.eslintrc_.
- **Material Icon Theme**: Adiciona Icones baseado na extensão do documento.
- **Prettier - Code formatter**: Essa extensão realmente aumenta a produtividade, através de um comando ou automaticamente,
  ela formata o código nos padrões configurados, definidos no editor, no _.editorconfig_ e _.eslintrc_

### Configurações

Para modificar as configurações do **VS Code** basta clicar no icone ⚙️ **> Settings > ... > Open settings.json** e substituir o json
completo **(O JSON DA DIRIETA)**.

Lembrando que utilizamos uma fonte de terceiros como padrão ([Fira Code](https://github.com/tonsky/FiraCode)), ela pode ser instalada seguindo este [tutorial](https://github.com/tonsky/FiraCode).

```
{
    "editor.fontFamily": "Fira Code",
    "editor.fontSize": 13,
    "editor.fontLigatures": true,
    "editor.lineHeight": 27,
    "editor.formatOnPaste": false,
    "editor.formatOnSave": false,
    "editor.renderLineHighlight": "none",
    "editor.minimap.enabled": false,

    "terminal.integrated.fontSize": 13,
    "terminal.integrated.shell.osx": "zsh",

    "workbench.colorTheme": "Dracula",
    "workbench.iconTheme": "material-icon-theme",
    "workbench.colorCustomizations": {
        "editorBracketMatch.background": "#16a085",
        "editorBracketMatch.border": "#16a085"
    },
    "workbench.sideBar.location": "left",

    "prettier.semi": true,
    "prettier.singleQuote": true,
    "prettier.trailingComma": "all",
    "prettier.eslintIntegration": true,
    "prettier.printWidth": 120,

    "explorer.confirmDragAndDrop": false,
    "window.zoomLevel": 0,
    "breadcrumbs.enabled": true,
}
```

### Teclas de Atalho

Teclas de atalho padronizadas agilizam quando estamos falando de trabalho em equipe, por isso, definimos algumas teclas de atalho que
acreditamos ser importantes estarem alinhadas para melhor produtividade enquanto trabalhamos juntos em algum projeto e/ou atividade.

Para modificar as teclas de atalho do **VS Code** basta clicar no icone ⚙️ **> Keyboard Shortcuts > keybindings.json** e substituir o json
completo **(O JSON DA DIRIETA)**.

No exemplo abaixo as teclas de atalho estão definidas em um MacBook, caso seu sistema operacional seja **Linux** ou **Windows** troque `cmd` por `ctrl`.

```
[
    {
        "key": "cmd+1",
        "command": "workbench.action.toggleSidebarVisibility"
    },
    {
        "key": "cmd+=",
        "command": "workbench.action.terminal.toggleTerminal"
    },
    {
        "key": "cmd+d",
        "command": "editor.action.copyLinesDownAction",
        "when": "editorTextFocus && !editorReadonly"
    },
    {
        "key": "shift+cmd+down",
        "command": "-editor.action.copyLinesDownAction",
        "when": "editorTextFocus && !editorReadonly"
    },
    {
        "key": "shift+cmd+d",
        "command": "editor.action.addSelectionToNextFindMatch",
        "when": "editorFocus"
    },
    {
        "key": "cmd+d",
        "command": "-editor.action.addSelectionToNextFindMatch",
        "when": "editorFocus"
    },
    {
        "key": "shift+cmd+l",
        "command": "editor.action.formatDocument",
        "when": "editorTextFocus && !editorReadonly"
    },
]
```

### Snippets

Snippets são palavras chaves que geram um código extenso, com intuito de aumentar a produtividade.

1. [Javascript](snippets/JAVASCRIPT.md)
