# UtilityFunction

## 概要

インスタンスの状態に全く依存しておらず、外部のオブジェクトに依存しているメソッド。

selfメソッドや変数を使っているか使っていないかの違いで、[FeatureEnvy](https://github.com/startup-technology/sideci-docs/blob/master/reek/FeatureEnvy.md)と同じ。

## 例

```ruby
class UtilityFunction
  def showcase(argument)
    argument.to_s + argument.to_i
  end
end
```

## 運用

`public_methods_only` オプションで public メソッドだけに制限ができます。

メソッドを小さくするために処理の一部を切り出した場合に起こる場合が多いため、`public_methods_only: true` に設定し、privateに移動するようにしてください。

```yaml
"app"
  UtilityFunction:
    public_methods_only: true
```

外部のクラスから参照されているメソッドである場合は、定義しているクラスを再考してみてください。

## 外部リンク

- [reek/Utility-Function.md](https://github.com/troessner/reek/blob/master/docs/Utility-Function.md)
