# 第3回デジタル手芸サークルハンズオン

## React

### 環境構築
### mac install
- 必要なもの
    - node.js version6以上
    - npm

- 参考資料
    - https://reactjs.org/docs/installation.html


#### アプリ製作
1. ターミナル起動  
1. 以下を打つ
```sh
npm install -g create-react-app
create-react-app my-app

cd my-app
npm start
```
※少し時間がかかる    
3. `npm start`をすると、localhost:3000で立ち上がる  
##### エラー
パーミッションなんとかと表示されたら
`sudo npm install -g create-react-app`




npm 5.2.0以上なら npx が使える
```sh
npx create-react-app my-app

cd my-app
npm start
```
#### Installing React
```sh
yarn init
yarn add react react-dom
```
or
```sh
npm init
npm install --save react react-dom
```
---

### windows install
分かりません  
windowsユーザーの方、ご記入お願いします。

---
## hello, world 　　index.jsにそのまま記入
1. my-app/src/index.js
2. 修正
```js
//ReactDOM.render(<App />, document.getElementById('root'));
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```
3. lolcalhost:3000でページリロード
1. hello, worldが表示される

## hello, world 　　App.jsを利用
1. my-app/src/App.js
1. class App extends Component の中
1. App-intro内を修正　brタグとhello, worldと記入
```js
<p className="App-intro">
    To get started, edit <code>src/App.js</code> and save to reload.<br />
    hello, world
</p>
```
4. lolcalhost:3000でページリロード
1. hello, worldが表示される

## hello, world 　　Hello Class作成
1. 自分のファイル階層/my-app % `touch src/Hello.js` と入力し、Hello.jsファイルを作成
1. Hello.jsを編集
```js
import React, { Component } from 'react';
import ReactDOM from 'react-dom';

class Hello extends Component{
    render() {
        return (
            <div className="Hello">
                <h1>Hello, world!</h1>
            </div>
        );
    }
}

export default Hello;
```
3. src/index.jsを編集
```sh
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import Hello from './Hello';
import registerServiceWorker from './registerServiceWorker';

//ReactDOM.render(<App />, document.getElementById('root'));
ReactDOM.render(
  <Hello />, document.getElementById('root')
);
registerServiceWorker();
```
4. lolcalhost:3000でページリロード
1. hello, worldが表示される
