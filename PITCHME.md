# **cloud-native**とは
なぜ  
クラウドネイティブなアプリケーションアーキテクチャ  
なのか

+++

### クラウドとは
コンピューティング、ネットワーキング、  
およびストレージリソースを  
オンデマンドのセルフサービス方式で柔軟に  
プロビジョニングおよび解放できる  
コンピューティング環境を意味します。  

---

### Cloud Native の恩恵
-1. リソース効率の向上により、少ないサーバーで同じ数のサービスが実行可能
-2. より高い開発スピードが実現可能となり、低リスクでの迅速なサービス改善
-3. マルチクラウドとハイブリッドクラウドの実現

+++

### 1.クラウドネイティブアプリケーションアーキテクチャの特徴
- Speed
- Safety
- Scale
- Mobile Applications and Client Diversity

---

### Speed
- 場所による優位性の減少
- リスクの軽減
  - リリースがあればあるほど、ミスからの復旧は早い
  - try & errorが可能に
- 顧客へのスピードの優位性

+++

### Safety
- Visibility
  - 
- Fault isolation
  - 障害の影響を受ける可能性のあるコンポーネントまたは機能の範囲を制限
  - マイクロサービス
- Fault tolerance
  - 
- Automated recovery
  - 
  
---

###  Scale
- システムの重要増加に伴い、マシンスペックを上げるなどで対応してきた
  - 季節イベントに伴うスパークに対応してきた結果、システムの使用率が低下
- 多数のより安価なコモディティマシンにわたってアプリケーションインスタンスを水平方向に拡張
  - 入手、配置が簡単
- 導入ハードルの容易さ

+++

### Mobile Applications and Client Diversity

---

## 2.Architectures
- Twelve-Factor Applications
- Microservices
- Self-Service Agile Infrastructure
- API-Based Collaboration
- Antifragility

+++

###  Twelve-Factor Applications
- I. コードベース (Codebase)
- II. 依存関係 (Dependencies)
- III. 設定 (Config)
- IV. バックエンドサービス (Backing Services)
- V. ビルド、リリース、ラン（Build, release, run）
- VI. プロセス (Processes)
- VII. ポートバインディング (Port binding)
- VIII. 並行性 (Concurrency)
- IX. 廃棄容易性 (Disposability)
- X. 開発/本番一致 (Dev/prod parity)
- XI. ログ (Logs)
- XII. 管理プロセス (Admin processes)

@size[2.5em]

---

I. コードベース (Codebase)
- 1 対 1で管理
II. 依存関係 (Dependencies)
- 明示的に
III. 設定 (Config)
- 環境差分はコードに含めず、環境変数として管理、設定
IV. バックエンドサービス (Backing Services)
- DBなどの補助的なサービスはリソースとしてアタッチする
V. ビルド、リリース、ラン（Build, release, run）
- コードをサービス提供可能な状態にするまで、明確にフェーズを分ける
- ロールバック、リスタートが高速に行える
VI. プロセス (Processes)
- ステートレスとすること
VII. ポートバインディング (Port binding)
- 自己完結し、ポートバインディングによって、結合すること
VIII. 並行性 (Concurrency)
- 
IX. 廃棄容易性 (Disposability)
- ライフサイクルを考慮すること
X. 開発/本番一致 (Dev/prod parity)
- 同じ環境となるように
XI. ログ (Logs)
- stdoutにログを吐き出し、イベントストリーム
XII. 管理プロセス (Admin processes)

---

### Microservices
- 機能の分割
  - 各機能間の調整が軽減
  - 各機能におけるメンテの容易さ
  - •モノリスは変更サイクルを結合し、独立したビジネス機能を必要に応じて展開できないため、イノベーションのスピードを妨げます。 •モノリスに埋め込まれているサービスは、他のサービスとは無関係に拡張できないため、効率的に負荷を計算するのははるかに困難です。 •組織に不慣れな開発者は、新しいチームに慣れ、新しいビジネスドメインを習得し、非常に大規模なコードベースに一度で慣れる必要があります。 これは、実際の生産性を達成する前に、通常3〜6か月の立ち上げ時間を増やすだけです。 •サンドボックスをさらに混雑させることで開発組織を拡張しようとすると、調整と通信のオーバーヘッドが高くなります。 •テクニカルスタックは長期にわたってコミットされています。 新技術の導入は、モノリス全体に悪影響を及ぼす可能性があるため、リスクが高すぎると見なされます。

+++

### Self-Service Agile Infrastructure
開発チームがアプリケーションおよびサービスの抽象化レベルで動作できるようにするクラウドプラットフォーム。インフラストラクチャレベルのスピード、安全性、および規模を提供します

---

### API-Based Collaboration
サービス間の対話を自動的に検証可能な契約として定義し、簡素化された統合作業によってスピードと安全性を可能にするアーキテクチャパターン。 

+++

### Antifragility
スピードとスケールによってシステムへのストレスが増大するにつれて、システムは対応能力を向上させ、安全性を高めます
