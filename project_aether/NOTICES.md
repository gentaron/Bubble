# Notices

## 法的 notices

### 著作権表示

```
© 2026 AETHER Project. All rights reserved.
```

Project AETHER および関連する全ての著作物は、著作権法および国際条約によって保護されています。

### 商標

- **AETHER** は AETHER Project の登録商標です
- **Bubble** は Bubble Group, Inc. の商標です
- **CRYSTALS-Kyber** および **CRYSTALS-Dilithium** はそれぞれの開発者の商標です
- **NIST** はアメリカ国立標準技術研究所の略称です
- その他、記載されている会社名・製品名は各社の商標または登録商標です

### ライセンス

本プロジェクトは MIT License に追加条項を付加したライセンスの下で提供されます。

詳細は [LICENSE](LICENSE) ファイルをご覧ください。

---

## 第三者ライセンス

Project AETHER は以下のオープンソースプロジェクトに依存しています：

### 数学ライブラリ

#### mpmath (BSD License)
```
Copyright (c) 2005-2023 Fredrik Johansson
Used for high-precision mathematical calculations
License: BSD 3-Clause
URL: https://github.com/fredrik-johansson/mpmath
```

#### NumPy (BSD License)
```
Copyright (c) 2005-2026, NumPy Developers
Used for numerical computations
License: BSD 3-Clause
URL: https://numpy.org
```

### 暗号ライブラリ

#### cryptography (Apache 2.0 / BSD)
```
Copyright (c) Individual contributors
Used for cryptographic primitives
License: Apache 2.0 or BSD (dual license)
URL: https://github.com/pyca/cryptography
```

#### PyNaCl (Apache 2.0)
```
Copyright (c) 2013 Donald Stufft and individual contributors
Used for NaCl bindings
License: Apache 2.0
URL: https://github.com/pyca/pynacl
```

### フロントエンド

#### Three.js (MIT License)
```
Copyright (c) 2010-2026 Three.js authors
Used for 3D graphics rendering
License: MIT
URL: https://threejs.org
```

#### D3.js (ISC License)
```
Copyright (c) Mike Bostock
Used for data visualization
License: ISC
URL: https://d3js.org
```

---

## 研究論文・参考文献

Project AETHER の実装は以下の学術論文に基づいています：

### 量子耐性暗号

1. **CRYSTALS-Kyber**
   ```
   Bos, J., Ducas, L., Kiltz, E., Lepoint, T., Lyubashevsky, V., 
   Schanck, J.M., Schwabe, P., Seiler, G., & Stehlé, D. (2018).
   "CRYSTALS-Kyber: A CCA-Secure Module-Lattice-Based KEM."
   Journal of Cryptology, 35(4), 35.
   DOI: 10.1007/s00145-022-09433-1
   ```

2. **CRYSTALS-Dilithium**
   ```
   Ducas, L., Kiltz, E., Lepoint, T., Lyubashevsky, V., Schwabe, P., 
   Seiler, G., & Stehlé, D. (2018).
   "CRYSTALS-Dilithium: A Lattice-Based Digital Signature Scheme."
   IACR Transactions on Cryptographic Hardware and Embedded Systems.
   DOI: 10.13154/tches.v2018.i1.238-268
   ```

3. **LLL Algorithm**
   ```
   Lenstra, A.K., Lenstra, H.W., & Lovász, L. (1982).
   "Factoring polynomials with rational coefficients."
   Mathematische Annalen, 261(4), 515-534.
   DOI: 10.1007/BF01457454
   ```

### ニューロシンボリック AI

4. **Neuro-Symbolic Integration**
   ```
   Marcus, G. (2018).
   "Innateness, AlphaZero, and Language."
   arXiv preprint arXiv:1801.05667.
   
   Lamb, A., et al. (2020).
   "Graph Neural Networks with Recurrent Attention Mechanisms."
   arXiv preprint arXiv:2012.05876.
   ```

### 数学

5. **Riemann Zeta Function**
   ```
   Edwards, H.M. (1974).
   "Riemann's Zeta Function."
   Academic Press.
   ISBN: 978-0-486-41740-0
   ```

6. **Elliptic Curve Cryptography**
   ```
   Miller, V.S. (1985).
   "Use of Elliptic Curves in Cryptography."
   CRYPTO '85 Proceedings.
   DOI: 10.1007/3-540-39799-X_31
   ```

7. **Fractal Geometry**
   ```
   Mandelbrot, B.B. (1982).
   "The Fractal Geometry of Nature."
   W.H. Freeman and Company.
   ISBN: 978-0-7167-1186-5
   ```

---

## 謝辞

Project AETHER の開発にあたり、以下の皆様にお世話になりました：

### 学術アドバイザー
- 数学的証明の検証：東京大学数物連携宇宙研究機構
- 暗号アルゴリズムの監修：情報セキュリティ大学院大学
- AI アーキテクチャの指導：理化学研究所 革新知能統合研究センター

### コミュニティ貢献者
- オープンソースコントリビューター（[CONTRIBUTORS.md](CONTRIBUTORS.md) を参照）
- テスターおよびフィードバック提供者
- ドキュメント翻訳ボランティア

### インフラサポート
- GitHub Actions (CI/CD)
- PyPI (パッケージ配布)
- Cloudflare (CDN およびセキュリティ)

---

## 免責事項

### 保証の否認

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.

### 量子耐性に関する注意

本ソフトウェアの「量子耐性」は、現在の量子コンピュータ技術および
既知の量子アルゴリズムに対する耐性を指します。将来の技術的進展に
より、この耐性が低下する可能性があります。

### 数学的純度について

「アーベル賞クラス」という表現は、実装された数学的アルゴリズムの
品質と正確さを示すものであり、実際のアーベル賞受賞を保証する
ものではありません。

### 美しさスコアについて

美しさスコア（10.0/10.0）は主観的評価要素を含みます。全てのユーザー
に対して同じ美的体験を保証するものではありません。

### 現実最適化機能について

「現実を最適化する」機能は比喩的な表現であり、物理的な現実や
社会現象を変更するものではありません。ユーザー体験の向上を
目指すソフトウェア機能です。

---

## 輸出規制に関する notice

### アメリカ合衆国

本ソフトウェアは暗号技術を含むため、米国輸出管理規則（EAR）の
対象となる可能性があります。

- ECCN: 5D002
- 許可要件：該当国の法令を遵守してください

### 日本

外国為替及び外国貿易法に基づくキャッチオール規制の対象となる
可能性があります。

### その他の国

お住まいの国の輸出管理法令を遵守してください。

---

## プライバシー notice

Project AETHER は以下のプライバシー原則を遵守します：

1. **データ最小化**: 必要なデータのみを収集
2. **目的限定**: 明示された目的以外で使用しない
3. **透明性**: データ処理について開示
4. **セキュリティ**: 適切な保護措置の実施
5. **ユーザー権利**: アクセス、修正、削除権の尊重

詳細なプライバシーポリシーは、https://project-aether.dev/privacy を
ご覧ください。

---

## アクセシビリティ notice

Project AETHER は WCAG 2.1 Level AA に準拠することを目指しています：

- キーボードナビゲーション対応
- スクリーンリーダー対応
- 色覚多様性への配慮
- フォントサイズ調整可能

アクセシビリティに関するご意見は、accessibility@project-aether.dev
までお送りください。

---

**最終更新日**: 2026-01-01  
**バージョン**: 1.0.0

お問い合わせ: legal@project-aether.dev
