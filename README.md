# BMP280-BME280sensorJavascript

BMP280 および BME280 を micro:bit で利用し、データを数値として表示・グラフ化するための JavaScript および HTML です。

🔗 [GitHub リポジトリはこちら](https://github.com/Tanagogedora/BMP280-BME280sensorJavascript/)

---

## 概要

このプロジェクトは、micro:bit に接続した BMP280 または BME280 センサから気温・気圧・湿度などのデータを取得し、  
Webブラウザ上でリアルタイムに数値表示・グラフ化するための仕組みを提供します。

Web Serial API を使って、micro:bit からのシリアルデータを受信・解析・表示する構成になっています。

---

## 特長

- micro:bit からのデータ送信（例: 温度、気圧、高度など）
- JavaScript によるリアルタイムデータ処理
- HTML 内でのデータ表示およびグラフ描画
- センサ種別に応じた柔軟な拡張

---

## 使用技術

- micro:bit（MakeCode）
- BMP280 / BME280 センサ
- JavaScript（ES6）
- HTML5
- Web Serial API
- Chart.js（グラフ描画）

---

## ファイル構成

/BME280気温気圧高度javascript外装.html // Web UI（グラフ＆数値表示　Javascript外装　GetData3.jsと併用）/BME280気温気圧高度javascript内装.html//Web UI（グラフ＆数値表示　Javascript内臓　HTML単独で利用できる） /GetData3.js // Web Serial + データ処理ロジック /LICENSE // MITライセンス /README.md // このファイル

---

## 使い方

1. micro:bit にセンサを接続し、MakeCode でセンサーデータをシリアル出力するプログラムを実装します。
2. 本プロジェクトの HTML ファイルをブラウザ（例：Edge）で開きます。
3. 「接続」ボタンを押して micro:bit を接続し、データを受信します。
4. ブラウザ上に数値とグラフが表示されます。
5. 「CSVログをダウンロード」ボタンを押すとログファイルがダウンロードできます。（デフォルト直近から300個前まで）
   注意点　「BME280気温気圧高度javascript外装.html」利用の際は同一ディレクトリに「GetData3.js」を置くこと
           気圧センサーが鋭敏なため、センサーの位置（高さ）の変化がなくても大きく値がずれることがあります。その際は「P0初期化」ボタンを押すと標高差計算の基準値になる気圧がリセットされます。
           なお初期状態で標高差は±1ｍ以内の誤差が出ることがわかっています。

---

## ライセンス

このプロジェクトは [MIT License](https://github.com/Tanagogedora/BMP280-BME280sensorJavascript/blob/main/LICENSE) のもとで公開されています。

自由に使用・改変・再配布できますが、著作権表示とライセンス文の記載が必要です。  
詳細は上記リンクまたはプロジェクト内の `LICENSE` ファイルをご確認ください。

© 2025 Tanagotti
