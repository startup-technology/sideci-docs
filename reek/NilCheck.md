# NilCheck

## 概要

- [Tell, Don't Ask](https://robots.thoughtbot.com/tell-dont-ask)の原理に違反しています。

## 例

```ruby
class Klass
  def nil_checker(argument)
    if argument.nil?
      puts "argument isn't nil!"
    end
  end
end
```

## 運用

対処するにはNullClassを作成する必要がありますが、RailsでNilCheckの対処のためだけにクラスを作るのはコストが高いため、基本的には無視して良いと思います。


```yml
"app":
  NilCheck:
    enabled: false
```

## 外部リンク

- [reek/Nil-Check.md](https://github.com/troessner/reek/blob/master/docs/Nil-Check.md)
