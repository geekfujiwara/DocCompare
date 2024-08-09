# ドキュメント比較アプリ

このアプリは、Power Apps を使用して作成されています。

2つのドキュメントをAI Builderを活用してその内容を比較し、その差異があった場合その影響について推定を行うアプリケーションです。

https://github.com/user-attachments/assets/a1f378b3-56b9-459d-8f61-40be57ae7c61

直接Azure OpenAI Searvice を必要とせず、AI Builder のAI プロンプト機能を利用して実現しています。

![image](https://github.com/user-attachments/assets/83045f46-7647-4e60-9aba-92af0c762771)


> [!Note]
> 利用して動いたよ、等の感想は是非[ギークフジワラのXのポスト](https://x.com/geekfujiwara/status/1821840041846731046)までお知らせください！

## 前提条件

- **ライセンス**
  - Power Apps Premium ライセンス 
  - AI Builder アドインライセンス (クレジットを基本ライセンスに付与されている分を超過して必要な場合)

## 制限事項

- AI Builder のAIプロンプトで利用しているモデルはGPT-4oです。そのため128,000トークンが上限です。
- 比較するドキュメントはPDF、または画像フォーマットである必要があります。

## ソリューションのインストール方法

1. **Power Apps ポータルにアクセス**
   - [Microsoft Power Apps 作成者ポータル](https://make.powerapps.com/)にログインします。

2. **ソリューションのインポート**
   - [本ソリューションのリリース](https://github.com/geekfujiwara/DocCompare/releases)からソリューションファイルを取得します。
   - Power Apps ポータルで「ソリューション」セクションに移動し、「インポート」ボタンをクリックして、ダウンロードしたソリューションファイルをアップロードします。
   - ラベルがないなどの警告が表示されたとしても問題ありません。

3. **すべてのカスタマイズの公開**
   - インポートしたソリューション内に入ります。**マネージド**のタブにソリューションは入っています。
   - そのまま、すべてのカスタマイズの公開を行います。
![image](https://github.com/user-attachments/assets/0ac7f4bb-287f-4e97-813b-d7452577f078)

## 利用手順

利用を検証するにあたって、[サンプルファイル](https://github.com/geekfujiwara/DocCompare/releases/tag/SampleFiles)を用意しています。契約書の比較を試すことができます。

1. **アプリの起動**
   - Power Appsホーム画面から「ドキュメント差異比較アプリ」を選択して起動します。
![image](https://github.com/user-attachments/assets/3f03c347-ea9f-4900-8c62-a9763d3bfec2)


2. **ドキュメントのアップロード**
   - アプリ内のアップロード機能を使用して、比較したい2つのドキュメントを選択します。
![image](https://github.com/user-attachments/assets/b3702dd8-0561-463b-b3b5-e96a1f12f058)

> [!Note]
> 左側はベースとなる資料としていますので、契約書の雛形や、過去の契約書、比較対象としたい仕様書などを読み込ませてください。

3. **比較**
   - 「比較」ボタンをクリックすることで、AI Builderが解析したテキストの内容を比較し、その影響についての推論結果が表示されます。

4. **内容の比較と推論のカスタマイズ**
   - こちらは任意ですが、自然言語で比較したい条件を追加することができます。
![image](https://github.com/user-attachments/assets/4afbd4c8-6bd9-4f40-b1f4-ddf758c1d49f)

5. **結果の保存**
   - 結果を保存できます。
   - 保存した結果は一覧で表示することができます。
![image](https://github.com/user-attachments/assets/8db587a5-07e8-4c3c-88e2-fff09e6e7d87)

ぜひご利用ください。
