# igroot-editor

igroot-editor is a react markdown editor


# Getting Started

### Install

```js
npm install igroot-editor -S
```

### Using igroot-editor

```js
import React, { Component } from 'react'
import ReactDOM from 'react-dom'
import Editor from 'igroot-editor'

class App extends Component {
  constructor() {
    super()
    this.state = {
      value: ''
    }
  }

  handleChange(value) {
    this.setState({
      value
    })
  }

  render() {
    const { value } = this.state
    return (
      <Editor 
       value={value}
       onChange={this.handleChange.bind(this)} 
       preview
       />
    )
  }
}

ReactDOM.render(
  <Editor />,
  document.getElementById('container')
)

```

### Api

#### props

| name | type | default | description |
| - | - | - | - |
| placeholder | String | 请输入内容... | 占位文本 |
| value | String| - |输入框内容 |
| preview | Boolean | false |默认开启编辑 |
| viewOnly | Boolean | false |只渲染md，不渲染编辑器 |
| lineNum | Boolean| true | 是否显示行号

#### events

| name | type | default | description |
| - | - | - | - |
| onChange | function(e) | - | 内容改变时回调 |
| onSave | function(e) | - | 保存时回调 |

#### hot key

| name | description |
| - | - |
| tab | 两个空格缩进 |
| ctrl+s | 保存 |
| ctrl+z | 上一步 |
| ctrl+y | 下一步 |
