# Snippets Javascript

## Lista de Snippets

- **statefull**: Cria um componente _statefull_ do React Native.
- **stateless**: Cria um componente _stateless_ do React Native.
- **styles**: Cria estrutura de _styles_ default do React Native. (Geralmente utilizada no styles.js)
- **normalize**: Cria estrutura de _styles_ com normalize do React Native. (Geralmente utilizada no styles.js)
- **eslint**: Cria as configurações do _eslint_ para React Native.
- **configureStore**: Cria as configurações da _store_ do _redux_ para React e React Native.
- **mapState**: Cria constante mapState.
- **mapActions**: Cria constante mapActions.
- **duck**: Cria estrutura _duck_ do Redux.
- **reactotronconfig**: Cria configuração do _Reactotron_ para React e React Native.

Para modificar os snippets de **Javascript** do **VS Code** basta clicar no icone ⚙️ > **User Snippets** > **javascript.json** e substituir o json completo.

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
  }
}
```
