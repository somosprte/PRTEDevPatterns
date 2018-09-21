# Snippets Javascript

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