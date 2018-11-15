
## 便利なpythonのコードをまとめていく

## ある変数の正体を調べたいとき： print, type, dir

print関数を使って、変数の値を調べることができます。
また、type(x)は、xの型を返す関数です。たとえば、次のプログラムを実行すると

```
x=4.2
print(x)
print(type(x))
```

次のような出力が帰ってきます。このことから、変数ｘの値は4.2で、その型は’float’であることがわかります。（floatは、pythonで実数を表現するのに通常つかわれる型です。）

```
4.2
<type 'float'>
```

さらに、dir(x)は、xの持っているメソッドを全て表示してくれます。

```
x="deep learning"
print(type(x))
print(dir(x))
```

```
<type 'str'>
['__add__', '__class__', '__contains__', '__delattr__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__getslice__', '__gt__', '__hash__', '__init__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '_formatter_field_name_split', '_formatter_parser', 'capitalize', 'center', 'count', 'decode', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'index', 'isalnum', 'isalpha', 'isdigit', 'islower', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
```

ここから、xは’str’型(文字列型)であること、またcapitalize, split, replaceなどのメソッドを持っていることがわかります。

メソッドや型の名前がわかれば、その使い方は「python str capitalize [検索]」などとして調べることができます。さっそく使ってみましょう。

```
x = ”deep learning”
print(x.capitalize())
print(x.split(" "))
print(x.replace("e","o"))
print(x.replace("e","n").split("n"))
```

は、次のような結果になります。

```
Deep learning
['deep', 'learning']
doop loarning
['d', '', 'p l', 'ar', 'i', 'g']
```

## 配列変数を調べたいとき： type, shape, dtype


