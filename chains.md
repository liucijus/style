**BAD** Chain logic group split
```scala
class Conversation(val contact: Contact, val count: Int, updated: Instant) {
    def asSiteContact = contact.details.asSiteContact(count)
      .copy(lastActivity = updated)
}
```

