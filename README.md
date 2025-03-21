# 求人情報テキスト解析プログラム

## 概要
このプロジェクトは、Yahoo!テキスト解析APIを使用して求人情報からキーフレーズを抽出し、その結果を様々な形式で可視化するプログラムです。

## 分析まとめブログ
https://medium.com/@GO2/テキスト解析webapiを使った特定求人のキートレンドを分析-74a966babf46

## 主な機能
1. キーフレーズ抽出
   - Yahoo!テキスト解析APIを使用して求人情報からキーフレーズを抽出
   - テキストの前処理（改行の削除、空白の正規化など）

2. 分析結果の可視化
   - ワードクラウドによる頻出キーフレーズの視覚化
   - 棒グラフによる上位キーフレーズの出現頻度表示
   - 各求人のTOP5キーフレーズとスコアの表形式での表示
   - キーフレーズの共起ネットワーク図の生成

## 必要なライブラリ
- pandas
- numpy
- matplotlib
- japanize_matplotlib
- networkx
- wordcloud
- requests

## 使用方法
1. Yahoo!テキスト解析APIのアプリケーションIDを取得し、`APPID`変数に設定
2. 分析対象の求人情報CSVファイルを用意（'求人内容'カラムが必要）
3. CSVファイルのパスを`pd.read_csv()`の引数に設定
4. プログラムを実行

## 出力結果
1. ワードクラウド
   - 頻出キーフレーズを視覚的に表示
   - フォントサイズが出現頻度を反映

2. 棒グラフ
   - 上位30件のキーフレーズの出現回数を表示
   - 頻度の高い順に表示

3. キーフレーズ分析表
   - 各求人ごとにTOP5のキーフレーズとそのスコアを表示
   - 求人内容の一部も併せて表示

4. 共起ネットワーク図
   - キーフレーズ間の関連性を視覚化
   - ノードの大きさが出現頻度を反映
   - ノードの色がスコアを反映

## 注意事項
- Yahoo!テキスト解析APIの利用には、アプリケーションIDが必要です
- 日本語フォントの設定が必要な場合は、`font_path`を適切に設定してください
- CSVファイルは適切なエンコーディングで保存されている必要があります 
