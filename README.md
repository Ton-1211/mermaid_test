# 課題
Mermaidを触ってみよう

マークダウンファイルを編集して、Mermaidで図を描いてみよう

# 取り組み方
* 本プロジェクトをforkしてください。
* README.mdを編集して、Mermaidを使いこなしてください
* できたらプルリクエストを出します

# 課題項目
## 流れ図
### 条件
- 開始と終了ノードをつける
- 条件分岐を組み込む
- 5ノード以上
- カッコいいほど高得点

## 解答
```mermaid
flowchart LR;
  A([開始]) --> B[/入力/];
  B --> C{判断};
  C -- 真 --> D[[サブルーチン]];
  D --> B;
  C -- 偽 --> F[表示];
  F --> E([終了]);
```

## シーケンス図
### 条件
- 3人以上
- メッセージをやり取りしない人がいないように
- 自己呼び出しを含むこと
- カッコいいほど高得点

## 解答
```mermaid
sequenceDiagram
    actor 太郎
    actor 花子
    actor 一郎
    太郎->>花子: おはよう！
    activate 花子
    花子-->>太郎: おはようございます!
    activate 一郎
    一郎->>花子: こんにちは!
    花子-->>一郎: こんにちは！
    deactivate 花子
    deactivate 一郎
```

## クラス図

### 条件
- 3つ以上
- 汎化と集約を含むこと
- カッコいいほど高得点

## 解答
```mermaid
classDiagram
    キャラクター o-- アイテム
    アイテム o-- 道具
    アイテム o-- 武器
    武器 <|-- 剣
    武器 <|-- 弓
    道具 <|-- つるはし
    道具 <|-- スコップ
    キャラクター o-- プレイヤー
    キャラクター　o-- 敵兵士
    敵兵士 <|-- 弓兵
    敵兵士 <|-- 歩兵
    
```
