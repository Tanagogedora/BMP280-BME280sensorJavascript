# BMP280-BME280sensorJavascript

BMP280 および BME280 を micro:bit で利用し、データを数値として表示・グラフ化するための JavaScript および HTML です。

🔗 [GitHub リポジトリはこちら](https://github.com/Tanagogedora/BMP280-BME280sensorJavascript/)

---

## 概要

このプロジェクトは、micro:bit に接続した BMP280 または BME280 センサから気温・気圧・湿度などのデータを取得し、Webブラウザ上でリアルタイムに数値表示・グラフ化するための仕組みを提供します。

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

### 🔹 HTMLファイル

- `/BME280気温気圧高度javascript外装.html`  
  Web UI（グラフ＆数値表示・JavaScript外装型、`GetData3.js` と併用）

- `/BME280気温気圧高度javascript内装.html`  
  Web UI（グラフ＆数値表示・JavaScript内蔵型、HTML単独で動作可）

### 🔹 JavaScriptファイル

- `/GetData3.js`  
  Web Serial API とデータ処理ロジック（外装HTMLと組み合わせて使用）

### 🔹 ドキュメント・ライセンス

- `/README.md`  
  プロジェクトの概要・使用方法・ライセンス情報など

- `/LICENSE`  
  MITライセンス全文

---

## 使い方

1. micro:bit にセンサを接続し、MakeCode でセンサーデータをシリアル出力するプログラムを実装します。
2. 本プロジェクトの HTML ファイルをブラウザ（例：Edge）で開きます。
3. 「接続」ボタンを押して micro:bit を接続し、データを受信します。
4. ブラウザ上に数値とグラフが表示されます。
5. 「CSVログをダウンロード」ボタンで、ログファイル（CSV形式）をダウンロードできます（デフォルトで最新300件を保存）。

### 🔸 注意点

-　BME280用で構築しましたがBMP280でも利用できます。ただし湿度のデータはありません。（BMP280は気温と気圧のセンサーのため）
- `BME280気温気圧高度javascript外装.html` を使用する場合は、`GetData3.js` を**同一ディレクトリに配置**してください。
- 気圧センサーは高感度なため、センサーの位置（高さ）の変化がなくても値に変動が生じることがあります。  
  その場合は「P0初期化」ボタンを押すと、標高差の計算基準となる気圧がリセットされます。
- 初期状態でも標高差には ±1m 程度の誤差が出ることがあります。

---

## ライセンス

このプロジェクトは [MIT License](https://github.com/Tanagogedora/BMP280-BME280sensorJavascript/blob/main/LICENSE) のもとで公開されています。

自由に使用・改変・再配布できますが、著作権表示とライセンス文の記載が必要です。  
詳細は上記リンクまたはプロジェクト内の `LICENSE` ファイルをご確認ください。

© 2025 Tanagotti

