**BAD** Hard to spot the structure
```scala
val foo = Foo(Bar(baz = Varoom(
  prop1 = "val", prop2 = "val2",
  prop3 = "val3),
  faz = Seq("one", "two")))
```
```scala
operations.query(contactById, Map(
  "site_id" -> getBytes(siteId),
  "contact_id" -> getBytes(contactId)
), ContactMapper)
```

**BETTER** Structure by logical groups
```scala
val foo = Foo(
  Bar(
    baz = Varoom(prop1 = "val1", prop2 = "val2", prop3 = "val3"),
    faz = Seq("one", "two")
  )
)
```
**GOOD** Flatten by extracting groups to vals
```scala
val baz = Varoom(prop1 = "val1", prop2 = "val2", prop3 = "val3")
val faz = Seq("one", "two")

val bar = Bar(baz = baz, faz = faz)

val foo = Foo(bar)
```

