# OWASP データセキュリティ Top 10 詳細

1. [インジェクション攻撃 (Injection Attacks)](#1-injection-attacks)
1. [不備のある認証とアクセス制御 (Broken Authentication and Access Control)](#2-broken-authentication-and-access-control)
1. [データ侵害 (Data Breaches)](#3-data-breaches)
1. [マルウェアおよびランサムウェア攻撃 (Malware and Ransomware Attacks)](#4-malware-and-ransomware-attacks)
1. [内部関係者の脅威 (Insider Threats)](#5-insider-threats)
1. [脆弱な暗号化 (Weak Cryptography)](#6-weak-cryptography)
1. [安全でないデータ処理 (Insecure Data Handling)](#7-insecure-data-handling)
1. [不十分なサードパーティセキュリティ (Inadequate Third-Party Security)](#8-inadequate-third-party-security)
1. [データインベントリとデータ管理 (Cyber Asset Inventory and Data Management)](#9-cyber-asset-inventory-and-data-management)
1. [データ保護規制の違反 (Non-Compliance with Data Protection Regulations)](#10-non-compliance-with-data-protection-regulations)

  

## 1. インジェクション攻撃 (Injection Attacks)

### 説明: インジェクション攻撃は攻撃者がアプリケーションの入力処理メカニズムの脆弱性を悪用して、悪意のあるコードやコマンドを注入することで発生します。これはデータ侵害、認可されていないアクセス、システムの完全な侵害につながる可能性があります。

### 事例: SQL インジェクションは攻撃者が悪意のある SQL コードをウェブアプリケーションの入力フィールドに挿入する一般的なタイプのインジェクション攻撃です。このコードはデータベースを操作し、機密データに認可されていないアクセスができます。

### CWE:

- CWE-89: SQL Injection
- CWE-77: Command Injection
- CWE-78: OS Command Injection
- CWE-79: Cross-Site Scripting (XSS)
- CWE-116: Improper Encoding or Escaping of Output

### 対策:

- パラメータ化クエリやプリペアドステートメントを使用して、SQL インジェクションを防ぎます。
- 入力バリデーションを実装し、ユーザー入力をサニタイズして、悪意のあるコードインジェクションをブロックします。
- ウェブアプリケーションファイアウォール (WAF) を採用して、インジェクション攻撃を検出してブロックします。


## 2. 不備のある認証とアクセス制御 (Broken Authentication and Access Control)

### 説明: 脆弱な認証メカニズムや不適切なアクセス制御によって、認可されていないユーザーが機密データへアクセスしたり、認可された権限を超えたアクションを実行する可能性があります。

### 事例: 脆弱なパスワード、安全でないセッション管理、不適切なユーザーロール割り当てによって、認可されていないユーザーが機密データにアクセスしたり、管理アクションを実行する可能性があります。

### CWE:

- CWE-287: Improper Authentication
- CWE-285: Improper Authorization
- CWE-798: Use of Hard-coded Credentials

### 対策:

- パスワードの複雑さ要件や定期的なパスワード更新など、強力なパスワードポリシーを適用します。
- 多要素認証 (MFA) を実装して、セキュリティ層を追加します。
- 最小権限の原則を適用し、ユーザーが必要なリソースにのみアクセスできるようにします。


## 3. データ侵害 (Data Breaches)

### 説明: データ侵害は機密データの認可されていない開示や窃取によって、その機密性、完全性、可用性が損なわれます。侵害は安全でないアプリケーション、誤って設定されたシステム、ソーシャルエンジニアリング攻撃などのさまざまな脆弱性によって発生する可能性があります。

### 事例: サイバー犯罪者が企業のウェブアプリケーションの脆弱性を悪用し、名前、住所、クレジットカード情報などの顧客の個人情報が含まれるデータベースにアクセスします。

### CWE:

- CWE-200: Information Exposure
- CWE-201: Information Exposure Through Sent Data
- CWE-311: Missing Encryption of Sensitive Data

### 対策:

- 定期的にソフトウェアやシステムにパッチ適用やアップデートを行い、脆弱性に対処します。
- 侵入検知および防御システム (IDPS) を導入し、認可されていないアクセス試行を検出してブロックします。
- 機密データを保存時と転送時の両方で暗号化し、認可されていないアクセスから保護します。


## 4. マルウェアおよびランサムウェア攻撃 (Malware and Ransomware Attacks)

### 説明: ウィルス、ワーム、ランサムウェアなどのマルウェアはシステムに感染して、データの完全性、可用性、機密性を損なう可能性があります。悪意のあるソフトウェアは電子メールの添付ファイル、悪意のあるウェブサイト、感染したソフトウェアなど、様々な攻撃ベクトルを通じて配信される可能性があります。

### 事例: ランサムウェアに感染した電子メールの添付ファイルをユーザーが知らずにダウンロードして開くと、ユーザーのファイルが暗号化され、その解除のために身代金を要求されます。

### CWE:

- CWE-94: Improper Control of Generation of Code
- CWE-120: Buffer Copy without Checking Size of Input
- CWE-506: Embedded Malicious Code

### 対策:

- 堅牢なアンチウィルスおよびアンチマルウェアソリューションを導入し、常に最新の状態に保ちます。
- 安全なブラウジングの習慣や、疑わしい添付ファイルを開いたり信頼できないウェブサイトにアクセスすることに危険性について、定期的に従業員を教育します。
- 重要なデータの最新のバックアップを維持して、ランサム攻撃の影響を軽減します。


## 5. 内部関係者の脅威 (Insider Threats)

### 説明: 内部関係者の脅威は従業員や請負業者などの認可された個人が意図的または非意図的に機密データを悪用または開示することが関係します。これにはデータの窃取、認可されていないアクセス、偶発的なデータ漏洩などがあります。

### 事例: 顧客データにアクセスできる従業員がその情報を競合他社に売却したり、誤って機密ファイルを間違った受信者に送信します。

### CWE:

- CWE-522: Insufficiently Protected Credentials
- CWE-502: Deserialization of Untrusted Data

### 対策:

- 堅牢なアクセス制御を導入し、従業員が職務に必要なデータおよびシステムにのみアクセスできるようにします。
- ユーザーアクティビティを監視およびログ記録して、疑わしい行動やデータ流出を検出します。
- 定期的にセキュリティ啓発トレーニングを実施して、セキュリティポリシーと認可されていないデータの取り扱いに関連するリスクについて従業員を教育します。


## 6. 脆弱な暗号化 (Weak Cryptography)

### 説明: 脆弱なアルゴリズムや不適切な鍵管理など、脆弱な暗号化のプラクティスによって、データが認可されていないアクセス、改竄、復号化されやすくなる可能性があります。

### 事例: 脆弱な暗号アルゴリズムを使用したり、簡単に推測できるデフォルトの暗号鍵を使用してデータベースにパスワードを保存します。

### CWE:

- CWE-327: Use of a Broken or Risky Cryptographic Algorithm
- CWE-326: Inadequate Encryption Strength
- CWE-323: Reusing a Nonce, Key Pair in Encryption

### 対策:

- 強力で最新の暗号アルゴリズムとプロトコルを使用します。
- 暗号鍵の安全な保管、ローテーション、配布など、適切な鍵管理を実施します。
- 業界のベストプラクティスに合わせて、暗号メカニズムを定期的にレビューして更新します。


## 7. 安全でないデータ処理 (Insecure Data Handling)

### 説明: 機密データの不適切な保管、転送、廃棄によって、不注意による流出や損失につながり、データの機密性と完全性を損なう可能性があります。

### 事例: 機密性の高い顧客情報を平文で保存したり、暗号化せずに安全でないネットワークで送信します。

### CWE:

- CWE-312: Cleartext Storage of Sensitive Information
- CWE-315: Cross-Site Scripting
- CWE-359: Exposure of Private Personal Information

### 対策:

- 強力なアクセス制御と暗号メカニズムを導入して、保存時と転送時のデータを保護します。
- 業界標準や規制に準拠するために、定期的にデータ処理手順を評価して更新します。
- 不要になったデータを安全に削除または廃棄するなど、安全なデータ廃棄プラクティスを実施します。

## 8. 不十分なサードパーティセキュリティ (Inadequate Third-Party Security)

### 説明: サードパーティベンダーやインテグレーションによるセキュリティ対策が不十分であることによって、データへの認可されていないアクセスに悪用される可能性がある脆弱性が生じます。

### 事例: ある企業では既知のセキュリティ脆弱性があるサードパーティコンポーネントを統合しているため、攻撃者がその脆弱性を悪用して企業のデータに認可されていないアクセスができるようになります。

### CWE:

- CWE-829: Inclusion of Functionality from Untrusted Control Sphere
- CWE-807: Reliance on Untrusted Inputs in a Security Decision

### 対策:

- 業務連携を行う前に、サードパーティベンダーのセキュリティ評価を徹底的に行います。
- ベンダーのリスク管理プログラムを導入し、サードパーティのセキュリティプラクティスを評価および監視します。
- セキュリティ要件や期待事項を含めるように契約書や同意書を定期的にレビューして更新します。

## 9. データインベントリとデータ管理 (Cyber Asset Inventory and Data Management)

### 説明: デジタル資産の不完全または不正確なインベントリと不適切なデータ管理プラクティスによって、データを効果的に防御し保護することが困難になります。

### 事例: 企業はハードウェア、ソフトウェア、データ資産の最新のインベントリを維持できず、未知のシステムや管理されていないシステムが攻撃者の標的になる可能性があります。

### CWE:

- CWE-200: Information Exposure
- CWE-522: Insufficiently Protected Credentials

### 対策:

- 定期的に資産の開示とインベントリ管理を実施して、すべてのデジタル資産の特定しカタログ化します。
- データ分類フレームワークを実装して、機密性に基づいてデータを分類し、それに応じて適切なセキュリティ制御を適用します。
- データの保存、アクセス制御、安全な廃棄プラクティスなど、データ管理ポリシーと手順を確立します。


## 10. データ保護規制の違反 (Non-Compliance with Data Protection Regulations)

### 説明: データ保護規制の違反とは機密データの保護、処理、保管に関して、適用されるデータ保護規制、業界標準、規制フレームワークで説明される要件を組織が満たしていないことを指します。その結果として法的罰則、風評被害、顧客の信頼の喪失となる可能性があります。

### 事例: 企業は顧客の個人情報を収集して保管していますが、適切な同意の取得、データ主体の権利の提供、必要なセキュリティ対策の導入など、欧州連合の一般データ保護規則 (GDPR) の要件を遵守できていません。

### CWE:

- CWE-259: Use of Hard-coded Password
- CWE-312: Cleartext Storage of Sensitive Information
- CWE-359: Exposure of Private Personal Information

### 対策:

- 組織の業務と取り扱うデータに適用される、関連するデータ保護規制と基準を理解します。
- データ処理アクティビティの徹底的な評価を実施して、インベントリについてコンプライアンス上のギャップを特定します。
- 適用される規制を確実に順守するために、堅牢なデータ保護ポリシー、手順、コントロールを開発および実装します。
- 規制の進展や新しい要件の発生に応じて、データ保護プラクティスを定期的にレビューして更新します。
- 従業員にトレーニングおよび啓発プログラムを提供し、従業員が自らの責任とコンプライアンスの重要性を理解できるようにします。
- 定期的な監査と評価を実施して、コンプライアンスの監視し、改善すべき領域を特定します。
- 法律顧問やデータ保護専門家と協力して、法的要件とベストプラクティスとの整合性を確保します。
- コンプライアンスの取り組みを実証するために、適切な文書と記録を維持します。
