ミミックメソッド
他の言語使用を偽装したメソッド。

例: 本来はメソッド呼び出しだが、あたかも代入のように書ける。

movie.title = "博士の異常な愛情"
と書けるが、内部では以下のように解釈されている。
movie.title=("博士の異常な愛情")

厳密には、イコールは代入ではなく引数に値を入れているだけということ。
