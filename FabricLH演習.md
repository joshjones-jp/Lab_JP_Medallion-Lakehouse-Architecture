---
title: Medallion Lakehouse アーキテクチャ入門🥉🥈🥇
permalink: index.html
layout: home
---
## Medallion アーキテクチャについて

メダリオン レイクハウス アーキテクチャ (一般に"メダリオン アーキテクチャ" と呼ばれます) は、組織がレイクハウス内のデータを論理的に整理するために使用する設計パターンです。 これは Fabric に推奨される設計アプローチです。

メダリオン アーキテクチャは、3 つの異なるレイヤー (ゾーン) で構成されています。 各レイヤーは、レイクハウスに保存されているデータの品質を示し、高いレベルは高い品質を表します。 この多層アプローチは、エンタープライズ データ製品にとっての信頼できる唯一のソースを構築するのに役立ちます。

重要なことは、メダリオンアーキテクチャは、データがレイヤーを通過する際に、原子性、一貫性、分離、耐久性（ACID）を保証することです。 生データから始まり、一連の検証と変換により、効率的な分析用に最適化されたデータが作られます。 メダリオン ステージには、ブロンズ (生)、シルバー (検証済み)、ゴールド (強化) の 3 つのステージがあります。

今回の演習の目標は Fabric のアーキテクチャをハンズオンでビルドして、グループで共有する事です。
人の作り方や好みによって、自然に図の見た目のバリエーションがあります。
最も大切なのは、**自分のFabricの理解を深める事です。**

## Azure Diagrams について
この演習では、無料ツールのAzure Diagramsを使用し、Fabricのアーキテクチャを説明する図を作成します。

Azure Diagramsは、Microsoft の公式なツールではありません。Microsoft の社員がアーキテクチャを説明するために作った便利なリソースです。
費用は一切かかりませんが、会社のセキュリティーおよびコンプライアンスのポリシーに従ってアカウントを作るか判断してください。
今日の演習では、アカウント無しでも実施ができますので、アカウント作成は受講者の自由となります。

Fabricだけではなく、他にもアーキテクチャの図は作成可能：
- Azure
- Power Platform・Dynamics 365
- マイクロソフト以外のベンダー（GCP、AWS等）

## Azure Diagramsへのアクセスと準備

先ずは以下のリンクをブラウザの別タブでアクセスしてください。
**Blank Canvas** を押します。

<!-- This link format lets us open in a seperate tab 😇 -->
<a href="https://azurediagrams.com/" target="_blank">https://azurediagrams.com</a>



<img src="images/AZD1.png" alt="Azure Diagramsメイン画面" style="width:950px; height:500px;">


ツールの案内と説明

### **任意**: アカウントの登録


今回の演習は、アカウントを登録せずに全てのタスクは完了可能です。
しかし、アカウントを持っている場合は以下のメリットあります：
- 作った Diagram を保存し、後で編集する
- Diagramを他のユーザーまたはコミュニティーに共有ができる
- 他のユーザーにプライベート（非公開）Diagram 共有とアクセス権限の設定（役割型）

<u>**サインアップする方法**</u>

1️⃣

右上の**Sign In**を押して、**Sign in or Create Accountを押します**

<img src="images/AZD8.png" alt="Azure Diagrams画面" style="width:950px; height:500px;">

2️⃣

**Don't have an account? Sign up now**を押します

3️⃣

以下の画面に、メールアドレスを入力して、メールアドレス確認が終わってからパスワードと名前を設定します。

<img src="images/AZD8-5.png" alt="Azure Diagrams画面" style="width:950px; height:500px;">


## Fabricのサンプル アーキテクチャ図を確認する

**1️⃣**

左下にある **Examples** を押します


<img src="images/AZD10.png" alt="Azure Diagrams画面" style="width:950px; height:500px;">

**2️⃣**


Examplesのウィンドウが開かれます。ウィンドウの上をマウスで掴んで(1)、サイズを調整します。
Fabricのサンプル図 **Lakehouse Architecture on Fabric**を探して、クリックします。(2)


<img src="images/AZD11.png" alt="Azure Diagrams画面" style="width:950px; height:500px;">

**3️⃣**

**Fabric Data Factory**と**Fabric Lakehouse**の間にある接続をマウスでかざして、統合の詳細が **Batch & Scheduled**となっている事を確認します。


<img src="images/AZD12.png" alt="Azure Diagrams画面" style="width:950px; height:500px;">

**4️⃣**


コミュニティーが提供している例もあります。**Community Diagrams**を押し、ブラウザのページ上検索（Ctrl+F)に「Fabric」を入力して、好きなサンプルを選びます。


<img src="images/AZD13.png" alt="Azure Diagrams画面" style="width:950px; height:500px;">

## Fabricのアーキテクチャ図を作成する


### 演習

1. lab 01-04 で実施した内容を Azure Diatrams を使用して作図しましょう

1. （option）1. の図をクローンし、lab 05-07 の内容を反映してみましょう

1. lab 01-04 の作図をメダリオンアーキテクチャとして拡張しましょう

### 回答例

1. [lab 01-04 の回答例へのリンク](./images/diagram-01-04.png)
   1. [Azure Diagrams](https://azurediagrams.com/D54ivtsh)
2. [lab 05-07 の回答例へのリンク](./images/diagram-05-07.png) 
   1. [Azure Diagrams](https://azurediagrams.com/e4F4s7l8)
3. [メダリオンアーキテクチャの回答例へのリンク](./images/diagram-medallion.png)
   1. [Azure Diagrams](https://azurediagrams.com/NhmRmML4)

## 図のエクスポートと共有

当日はTeamsを使っているか確認

## リソース

- [Microsoft Fabric でメダリオン Lakehouse アーキテクチャを実装](https://learn.microsoft.com/jp-ja/fabric/onelake/onelake-medallion-lakehouse-architecture)
- [Microsoft Fabric のグリーンフィールド レイクハウス](https://learn.microsoft.com/ja-jp/azure/architecture/example-scenario/data/greenfield-lakehouse-fabric)
- [Microsoft Fabric 開発ガイド](https://speakerdeck.com/ryomaru0825/microsoft-fabric-kai-fa-gaido?slide=31)
