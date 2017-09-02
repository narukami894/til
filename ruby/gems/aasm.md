aasmでは、そのイベントを発生できるかどうかを
`may_#{イベント名}`というメソッドで判定することができる。


aasm/lib/aasm/base.rb
```
# an addition over standard aasm so that, before firing an event, you can ask
# may_event? and get back a boolean that tells you whether the guard method
# on the transition will let this happen.
safely_define_method klass, "may_#{name}?", ->(*args) do
  aasm(aasm_name).may_fire_event?(event, *args)
end
```

aasm/lib/aasm/instance_base.rb
```
def may_fire_event?(name, *args)
  if event = @instance.class.aasm(@name).state_machine.events[name]
    !!event.may_fire?(@instance, *args)
  else
    false # unknown event
  end
end
```
