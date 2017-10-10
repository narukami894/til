空の配列に`each`や`map`してもnilになるだけでエラーにならない。
```
[].map { |i| i }
```
ちなみに`Mongoid::Criteria`の空のCriteriaでもエラーにならない。
