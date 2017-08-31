obj.methodsでメソッド一覧が出せる

インスタンス変数はオブジェクトに住んでいる
メソッドはクラスに住んでいる

String.instance_methods == 'abc'.methods

'hello'.class => String
String.class => Class

Class.superclass => Module
ClassはModuleを継承している

Class < Module < Object < BasicObject

SomeClass < Object < BasicObject

クラスもただのオブジェクト

クラス名はただの定数

定数は::を使って指定して呼び出せる
