---

layout: col-sidebar
title: OWASP Data Security Top 10
tags: cloud data datasecurity security top10 data-security cloud-data cloud-data-security roadmap news acknowledgments
level: 2
type: documentation
pitch: 保存時や移動時にデータを保護するためのベストプラクティスガイドです。このガイドは機密情報や個人を識別できる情報の保存や移動に関する最も主要なセキュリティリスク、関連する課題、それらを克服する方法についての情報を提供します。

---

## 概要

データは多くの組織が保有する最も重要な資産ですが、データセキュリティが最優先ではないことがよくあります。データは本質的に企業が保護すべき唯一の資産です。このガイドは機密情報や個人を識別できる情報の保存や移動に関する最も主要なセキュリティリスク、関連する課題、それらを克服する方法についての情報を提供します。

## 目的

OWASP データセキュリティ Top 10 は最も一般的なデータセキュリティの脆弱性がもたらす結果についての意識を高め、それらを特定して保護するための基本的なテクニックを提供したいと考えています。

## 参加するには

貢献するにはセキュリティ専門家やプログラマーである必要はありません。参加するにはプロジェクトリーダーに連絡してください。提案や意見を歓迎します。貢献できる方法は以下の通りです。

 * データセキュリティの課題を理解している組織や個人を積極的に探しています。
 * プロジェクトに貢献した個人および組織は謝辞ページに掲載されます。

## データセキュリティ Top 10 2023

* **[DATA1:2023 - インジェクション攻撃 (Injection Attacks)][DATA1:2023]**

  認可されていない個人が脆弱性を悪用して悪意のあるコードやコマンドを注入することによって、データの完全性や機密性を侵害します。 [続きを読む][DATA1:2023]

* **[DATA2:2023 - 不備のある認証とアクセス制御 (Broken Authentication and Access Control)][DATA2:2023]**

  脆弱な認証メカニズム、不適切なアクセス制御、誤ったパーミッション設定によって、機密データへの認可されていないアクセスができます。 [続きを読む][DATA2:2023]

* **[DATA3:2023 - データ侵害 (Data Breaches)][DATA3:2023]**

  機密データの認可されていない開示や窃取によって、その機密性が損なわれ、法的な影響や風評被害につながる可能性があります。 [続きを読む][DATA3:2023]

* **[DATA4:2023 - マルウェアおよびランサムウェア攻撃 (Malware and Ransomware Attacks)][DATA4:2023]**

  多くの場合、フィッシング攻撃やパッチが適用されていないソフトウェア脆弱性によって、悪意のあるソフトウェアを感染し、データの可用性、機密性、完全性を損なう可能性があります。 [続きを読む][DATA4:2023]

* **[DATA5:2023 - 内部関係者の脅威 (Insider Threats)][DATA5:2023]**

  従業員や請負業者などの認可されたユーザーによる悪意のあるアクションや意図しないアクションによって、機密データへの認可されていないアクセス、悪用、流出につながります。 [続きを読む][DATA5:2023]

* **[DATA6:2023 - 脆弱な暗号化 (Weak Cryptography)][DATA6:2023]**

  脆弱なアルゴリズム、不適切な鍵管理、暗号化の欠如など、不適切な暗号化のプラクティスによって、認可されていないアクセスや改竄に対してデータが脆弱になります。 [続きを読む][DATA6:2023]

* **[DATA7:2023 - 安全でないデータ処理 (Insecure Data Handling)][DATA7:2023]**

  機密データの不適切な保管、転送、廃棄によって、不注意による流出や損失につながります。 [続きを読む][DATA7:2023]

* **[DATA8:2023 - 不十分なサードパーティセキュリティ (Inadequate Third-Party Security)][DATA8:2023]**

  サードパーティベンダーやインテグレーションによるセキュリティ対策が不十分であることによって、データへの認可されていないアクセスに悪用される可能性がある脆弱性が生じます。 [続きを読む][DATA8:2023]

* **[DATA9:2023 - データインベントリとデータ管理 (Data Inventory and Data Management)][DATA9:2023]**

  デジタル資産の不完全または不正確なインベントリと不適切なデータ管理プラクティスによって、データを効果的に防御し保護することが困難になります。 [続きを読む][DATA9:2023]

* **[DATA10:2023 - データ保護規制の違反 (Non-Compliance with Data Protection Regulations)][DATA10:2023]**

  適用されるデータ保護規制、業界標準、法的要件を遵守しないことによって、組織は法的責任や風評被害にさらされます。 [続きを読む][DATA10:2023]

## ライセンス

**OWASP データセキュリティプロジェクトのドキュメントはフリーに使用できます。**

OWASP データセキュリティプロジェクトは [Creative Commons Attribution-ShareAlike 4.0 license][license] の下でライセンスされていますので、あなたはこの著作物を複製、配布、送信できますし、翻案や商業的な使用が可能ですが、すべて帰属表示が必要です。この著作物を変更、変形、構築する場合、結果として得られる著作物はこの著作物と同じまたは類似のライセンスの下でのみ配布可能です。






[license]: https://creativecommons.org/licenses/by-sa/4.0/
[DATA1:2023]: https://owasp.org/www-project-data-security-top-10/1-injection-attacks/
[DATA2:2023]: https://owasp.org/www-project-data-security-top-10/2-broken-authentication-and-access-control/
[DATA3:2023]: https://owasp.org/www-project-data-security-top-10/3-data-breaches/
[DATA4:2023]: https://owasp.org/www-project-data-security-top-10/4-malware-and-ransomware-attacks/
[DATA5:2023]: https://owasp.org/www-project-data-security-top-10/5-insider-threats/
[DATA6:2023]: https://owasp.org/www-project-data-security-top-10/6-weak-encryption/
[DATA7:2023]: https://owasp.org/www-project-data-security-top-10/7-insecure-data-handling/
[DATA8:2023]: https://owasp.org/www-project-data-security-top-10/8-inadequate-thirdparty-security/
[DATA9:2023]: https://owasp.org/www-project-data-security-top-10/9-data-inventory-and-data-management/
[DATA10:2023]: https://owasp.org/www-project-data-security-top-10/10-non-compliance-and-data-protection-regulations/
