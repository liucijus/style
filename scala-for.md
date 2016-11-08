**BAD** `for` comprehension forms a separate logical group
```scala
  Response(for {
      details <- snapshop.details
      contact <- contacts.get(details.contactId)
      activity <- activities.get(contact.id)
    } yield Payload(activity))
```

**GOOD** `for` comprehension as a multiple line logical group
```scala
  Response(
    for {
      details <- snapshop.details
      contact <- contacts.get(details.contactId)
      activity <- activities.get(contact.id)
    } yield Payload(activity)
  )
```
**GOOD** `for` result extracted to reduce cyclomatic complexity
```scala
  val result = for {
    details <- snapshop.details
    contact <- contacts.get(details.contactId)
    activity <- activities.get(contact.id)
  } yield Payload(activity)

  Result(result)

```
