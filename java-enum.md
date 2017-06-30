**BAD** Broken logical group
```java
enum State {
  READ, WRITE,
  PAUSE, STOP
}
```
**GOOD** Consistent logical group on the same line
```java
enum State {
  READ, WRITE, PAUSE, STOP
}
```
**GOOD**
Consistently broken per logical item in the group
```java
enum State {
  READ, 
  WRITE,
  PAUSE, 
  STOP
}
```




