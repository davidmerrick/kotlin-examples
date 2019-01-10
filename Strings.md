# Strings

## String replacement

In Java, this method can be confusing:

```java
"one.two".replaceAll(".", "*");
// Returns "*******", because replaceAll expects a regex as the first argument
```

Kotlin improves on this with `replace()`, which takes a String as the first argument, and an overloaded method which takes a regex:
```kotlin
"one.two".replace(".", "*")
// Returns "one*two"

"one.two".replace(".".toRegex(), "*")
// Returns "*******"
```
