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
// Place your key bindings in this file to overwrite the defaults
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

Para modificar os snippets de **Javascript** do **VS Code** basta clicar no icone ⚙️ **> User Snippets > javascript.json** e substituir o json
completo.

**javascript.json**
```
{
  "component": {
    "prefix": "statefull",
    "body": [
      "import React, { Component } from 'react';",
      "",
      "import { View } from 'react-native';",
      "",
      "// import styles from './styles';",
      "",
      "export default class ${1:MyComponent} extends Component {",
      "  render() {",
      "    return (",
      "      <View />",
      "    );",
      "  }",
      "}",
      ""
    ],
    "description": "Create react-native component"
  },
  "componentStateless": {
    "prefix": "stateless",
    "body": [
      "import React from 'react';",
      "",
      "import { View } from 'react-native';",
      "",
      "// import styles from './styles';",
      "",
      "const ${1:MyComponent} = () => (",
      "  <View />",
      ");",
      "",
      "export default ${1:MyComponent};",
      ""
    ],
    "description": "Create react-native stateless component"
  },
  "styles": {
    "prefix": "styles",
    "body": ["import { StyleSheet } from 'react-native';", "", "export default StyleSheet.create({", "  ${1}", "});"],
    "description": "Create react-native Style file"
  },
  "normalize": {
    "prefix": "normalize",
    "body": [
      "import StyleSheetNormalize from 'react-native-stylesheet-normalize';",
      "",
      "export default StyleSheetNormalize.create({",
      "  ${1}",
      "});"
    ],
    "description": "Create react-native Style file"
  },
  "proptypes": {
    "prefix": "proptypes",
    "body": ["static propTypes = {", "  ${1}", "};"],
    "description": "Create component propTypes"
  },
  "defaultprops": {
    "prefix": "defaultprops",
    "body": ["static defaultProps = {", "  ${1}", "};"],
    "description": "Create component defaultProps"
  },
  "constructor": {
    "prefix": "ctor",
    "description": "Create constructor method on Stateful Component",
    "body": ["constructor(props) {", "  super(props);", "  this.state = {};", "}"]
  },
  "render": {
    "prefix": "render",
    "body": ["render() {", "  return (", "    ${1:<View />}", "  );", "}"],
    "description": "Create render method"
  },
  "eslint": {
    "prefix": "eslint",
    "body": [
      "{",
      "  \"parser\": \"babel-eslint\",",
      "  \"env\": {,",
      "    \"browser\": true,",
      "    \"jest\": true",
      "  },",
      "  \"plugins\": [",
      "    \"react-native\",",
      "    \"jsx-a11y\",",
      "    \"import\",",
      "  ],",
      "  \"extends\": [",
      "    \"airbnb\",",
      "    \"plugin:react-native/all\"",
      "  ],",
      "  \"rules\": {",
      "    \"react/jsx-filename-extension\": [\"error\", { \"extensions\": [\".js\", \".jsx\"] }],",
      "    \"global-require\": \"off\",",
      "    \"no-console\": \"off\",",
      "    \"import/prefer-default-export\": \"off\",",
      "    \"no-unused-vars\": [\"error\", {\"argsIgnorePattern\": \"^_\"}]",
      "  },",
      "  \"settings\": {",
      "    \"import/resolver\": {",
      "      \"babel-module\": {}",
      "    }",
      "  },",
      "  \"globals\": {",
      "    \"__DEV__\": true",
      "  }",
      "}"
    ],
    "description": "Create eslint file config"
  },
  "reduxSetup": {
    "prefix": "reduxSetup",
    "body": [
      "import { combineReducers } from 'redux';",
      "",
      "/* Reducers */",
      "// import navReducer from 'navigation/reducer';",
      "",
      "import configureStore from './configureStore';",
      "// import rootSaga from './sagas';",
      "",
      "export default () => {",
      "  const rootReducer = combineReducers({",
      "    // nav: navReducer,",
      "  });",
      "",
      "  return configureStore(rootReducer, rootSaga);",
      "};",
      ""
    ],
    "description": "Create Redux Setup file"
  },
  "configureStore": {
    "prefix": "configureStore",
    "body": [
      "import { createStore, applyMiddleware, compose } from 'redux';",
      "",
      "export default (rootReducer) => {",
      "  const middleware = [];",
      "  const enhancers = [];",
      "",
      "  /* Saga */",
      "  // const sagaMonitor = __DEV__ ? console.tron.createSagaMonitor() : null;",
      "  // const sagaMiddleware = createSagaMiddleware({ sagaMonitor });",
      "  // middleware.push(sagaMiddleware);",
      "",
      "  enhancers.push(applyMiddleware(...middleware));",
      "",
      "  /* Store */",
      "  const createAppropriateStore = __DEV__ ? console.tron.createStore : createStore;",
      "  const store = createAppropriateStore(rootReducer, compose(...enhancers));",
      "",
      "  /* Run Saga */",
      "  // sagaMiddleware.run(rootSaga);",
      "",
      "  return store;",
      "};",
      ""
    ],
    "description": "Create configureStore file"
  },
  "reduxComponent": {
    "prefix": "reduxComponent",
    "body": [
      "import React, { Component } from 'react';",
      "",
      "import { View } from 'react-native';",
      "",
      "import { connect } from 'react-redux';",
      "",
      "// import styles from './styles';",
      "",
      "class ${1:MyComponent} extends Component {",
      "  render() {",
      "    return (",
      "      <View />",
      "    );",
      "  }",
      "}",
      "",
      "const mapStateToProps = state => ({});",
      "",
      "const mapDispatchToProps = dispatch => ({});",
      "",
      "export default connect(mapStateToProps, mapDispatchToProps)(${1:MyComponent});",
      ""
    ],
    "description": "Create react-native Redux component"
  },
  "reduxComponentStateless": {
    "prefix": "reduxComponentStateless",
    "body": [
      "import React from 'react';",
      "",
      "import { View } from 'react-native';",
      "",
      "import { connect } from 'react-redux';",
      "",
      "// import styles from './styles';",
      "",
      "const ${1:MyComponent} = () => (",
      "  <View />",
      ");",
      "const mapStateToProps = state => ({",
      "",
      "});",
      "",
      "const mapDispatchToProps = dispatch => ({",
      "",
      "});",
      "",
      "export default connect(mapStateToProps, mapDispatchToProps)(${1:MyComponent});",
      ""
    ],
    "description": "Create react-native stateless Redux component"
  },
  "mapState": {
    "prefix": "mapState",
    "body": ["const mapState = state => ({", "  ${1}", "});"],
    "description": "Create redux mapState"
  },
  "mapActions": {
    "prefix": "mapActions",
    "body": ["const mapActions = dispatch => bindActionCreators(${1}, dispatch);"],
    "description": "Create redux mapActions"
  },
  "duck": {
    "prefix": "duck",
    "body": [
      "import { createReducer, createActions } from 'reduxsauce';",
      "import Immutable from 'seamless-immutable';",
      "",
      "/* Types & Action Creators */",
      "",
      "const { Types, Creators } = createActions({",
      "// actionType: ['dataPassed'],",
      "});",
      "",
      "export const ${1:name}}Types = Types;",
      "export default Creators;",
      "",
      "/* Initial State */",
      "",
      "export const INITIAL_STATE = Immutable({",
      "// data: [],",
      "});",
      "",
      "/* Reducers */",
      "",
      "// export const reducer = state =>",
      "//   state.merge({ data: [] });",
      "",
      "/* Reducers to types */",
      "",
      "export const reducer = createReducer(INITIAL_STATE, {",
      "// [Types.ACTION_TYPE]: reducer,",
      "});",
      ""
    ],
    "description": "Create react-native duck module"
  },
  "reactotronconfig": {
    "prefix": "reactotronconfig",
    "body": [
      "import Reactotron from 'reactotron-react-native';",
      "",
      "if (__DEV__) {",
      "  const tron = Reactotron",
      "    .configure()",
      "    .useReactNative()",
      "    .connect();",
      "",
      "  tron.clear();",
      "",
      "  console.tron = tron;",
      "}",
      ""
    ],
    "description": "Create Reactotron Config"
  },
  "moduleResolver": {
    "prefix": "moduleResolver",
    "body": [
      "{",
      "  \"presets\": [\"react-native\"],",
      "  \"plugins\": [ ",
      "    [",
      "      \"module-resolver\",",
      "      {",
      "        \"cwd\": \"babelrc\",",
      "        \"root\": [\"./src\"],",
      "        \"extensions\": [\".js\", \".ios.js\", \".android.js\"]",
      "      }",
      "    ]",
      "  ]",
      "}"
    ],
    "description": "Create Module Resolver config"
  },
  "apisauce": {
    "prefix": "api",
    "body": [
      "import { create } from 'apisauce';",
      "",
      "const api = create({",
      "  baseURL: '${1:http://localhost:3000}',",
      "});",
      "",
      "export default api;",
      ""
    ],
    "description": "Create APISauce Config"
  }
}

```
