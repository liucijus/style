**BAD** Fields in the same logical group given uneven placement
```scala
case class Activity(contact: Contact,
                    created: Instant,
                    payload: String)
```
**GOOD** Fields in the same logical group on the same line as class declaration
```scala
case class Activity(contact: Contact, created: Instant, payload: String)
```
*GOOD** Fields on separate line 
```scala
case class Activity(
  contact: Contact, created: Instant, payload: String
)
```
**GOOD** Fields in the same logical group per separate line
```scala
case class Activity(
  contact: Contact, 
  created: Instant, 
  payload: String
)
```
**BAD** Closing brace part of wrong logical group
```scala
case class Activity(
  contact: Contact, 
  created: Instant, 
  payload: String)

```
