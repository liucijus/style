**BAD** Chain logic group split
```scala
  val asSiteContact = contact.details.asSiteContact(count)
    .copy(lastActivity = updated)
```
**GOOD** Chaining on the same line
```scala
  val asSiteContact = contact.details.asSiteContact(count).copy(lastActivity = updated)
```
**GOOD** Chaining calls line per method
```scala
  val asSiteContact = contact
    .details
    .asSiteContact(count)
    .copy(lastActivity = updated)
```

