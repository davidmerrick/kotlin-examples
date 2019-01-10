# Strings

## String replacement

In Java, this method can be confusing:

```java
"one.two".replaceAll(".", "*");
// Returns "*******", because replaceAll expects a regex as the first argument
```

Kotlin improves on this with two methods:
```kotlin
"one.two".replace(".", "*")
// Returns "one*two"

"one.two".replace(".".toRegex(), "*")
// Returns "*******"
```
