# Reek

- [コードの臭い(Code smell)](https://ja.wikipedia.org/wiki/%E3%82%B3%E3%83%BC%E3%83%89%E3%81%AE%E8%87%AD%E3%81%84)検出器。

## 運用
- Reekの指摘はワーニングと扱う。状況により修正するか、無視するかを判断する。
- 無視をする場合は抑止コメントを残す。 `:reek:NestedIterators`
