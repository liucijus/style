**BAD** Logical group mixed with braces
```scala
val map = Map("key1" -> "val1",
  "key2" -> "val2")
```
**BAD** First logical group member out of the group
```scala
val map = Map("key1" -> "val1",
  "key2" -> "val2",
  "key3" -> "val3"
)
```
**BAD** Wrong split
```scala
val map = Map(
  "key1" -> "val1", "key2" -> "val2",
  "key3" -> "val3", "key4" -> "val4"
)
```
**GOOD** parameters on the same as constructor
```scala
val map = Map("key1" -> "val1", "key2" -> "val2", "key3" -> "val3", "key4" -> "val4")
```

**GOOD** parameters as logical group have their own line
```scala
val map = Map(
  "key1" -> "val1", "key2" -> "val2", "key3" -> "val3", "key4" -> "val4"
)
```
**GOOD** each parameter on a separate line
```scala
val map = Map(
  "key1" -> "val1",
  "key2" -> "val2", 
  "key3" -> "val3",
  "key4" -> "val4"
)
```

