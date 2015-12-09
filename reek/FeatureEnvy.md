## 概要

メソッドが自分の所属しないクラスに興味（浮気心）があるようです。

他のクラスへの参照が多く、変更に弱いプログラムになっています。

## 例

```ruby
class Warehouse
  def sale_price(item)
    (item.price - item.rebate) * @vat
  end
end
```

## 運用

できる限り修正したほうが望ましいですが、参照先がサードパーティのライブラリであったり、修正が難しい場合があります。
開発状況を見て修正するべきかその都度判断するのが望ましいと思われます。

参照先のライブラリの変更に弱いため、テストを書くように心がけてください。

## 外部リンク

- [reek/Feature-Envy.md](https://github.com/troessner/reek/blob/master/docs/Feature-Envy.md)
