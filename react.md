## 用語

#### JSX

UIの記述をHTMLのように書くことができるJavaScriptの拡張構文
Babelやswcを通してJavaScriptへ変換される
関数が戻り値でJSX要素を返す
```jsx
const MyHello = () => {
  const hoge = 'Tada';
  
  return (<div>Hello ${hoge}</div>);
}
```

#### React
UIを構築するためのJavaScriptライブラリ
「このデータのときは、このUI」ということを書くと、データが変わったときに変わった部分だけ自動で更新してくれる。DOM操作などを一からせずにするこちができる
dom, jqueryではデータが変わったときに連動する箇所を1つずつ手動で更新する必要があった

#### コンポーネント
UIを構築するための再利用可能なUIの部品
関数コンポーネント
JavaScript関数の形式で記述されるコンポーネント
コンポーネントには旧式のクラスコンポーネントと現在主流の関数コンポーネントがある

#### クラスコンポーネント
旧式の書き方、クラスを使う
tbw
#### props
**Propertiesの略、属性**
HTML タグのアトリビュート 属性 にあたるもの
親コンポーネントから渡されるコンポーネントの引数

#### children
reactのコンポーネントの小要素
propsのchildren要素としてアクセスできる

#### state
コンポーネントが内部に持つ変化するデータ 状態
stateが変わると画面が最新の状態に再レンダリングがかかる

イベントハンドラ
クリックや入力などのイベントが起こったときにreactが呼び出す関数

```jsx
const MyButton = () => {
  const handleClick = (e: React.MouseEvent<HTMLButtonElement>) => {
	  console.log(e.target.value);
  }
  
  return (
	  <div>
		  <button onClick={handleClick}>clicked</butoton>
	  </div>
  )
}
```