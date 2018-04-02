# react-native-folder-structure
## General Structure
```
MyProject
├── __tests__
├── android
├── ios
├── src
│   └── config
│   │      └── index.js
│   └── components
│   │      └── MyComponent
│   │      │     └── MyComponent.js
│   │      │     └── MyComponentStyle.js
│   │      └── index.js
│   └── redux
│   │    └── actions
│   │    │  └── index.js
│   │    └── reducers
│   │    │      └── index.js
│   │    └── store
│   │           └── index.js
│   ├── resources
│   ├── screens
│   │      └── index.js
│   ├── RootNavigator.js
│   └── App.js
├── app.json
├── index.js
├── package.json
├── package-lock.json
```

## Imports/Exports
Each index.js file should export everything inside the respective folder.
If the folder contains an Component, The component should be export inside "{ }"
Example:

MyComponent.js 
```
import React, {Component } from 'react'
import styles from './MyComponent'

class MyComponent extends Component{

  render(){
    return(
      
    )
  }
}

export { MyComponent };

```
index.js
```
export * from './MyComponent/MyComponent'
```

importing: 
```
import { MyComponent } from '../../components'
```
