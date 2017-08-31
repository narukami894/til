`[{0=>{:name=>nil}}, {1=>{:name=>nil}}, {2=>{:name=>"aa"}}]`
を
`{0=>{:name=>nil},1=>{:name=>nil}, 2=>{:name=>"aa"}}`
に変換するにはどうすれば短く書ける？

`inject(:update)`
可読性が高く速いが、破壊的で危険

`inject(:merge)`
可読性が高いが、遅い

`map(&:flatten).to_h`
速いが、可読性が低い
