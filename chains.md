**BAD** Chain logic group split
```scala
  def asSiteContact = contact.details.asSiteContact(count)
    .copy(lastActivity = updated)
```
**GOOD** Chaining on the same line
```scala
  def asSiteContact = contact.details.asSiteContact(count).copy(lastActivity = updated)
```
**GOOD** Chaining calls line per method
```scala
  def asSiteContact = contact
    .details
    .asSiteContact(count)
    .copy(lastActivity = updated)
```

