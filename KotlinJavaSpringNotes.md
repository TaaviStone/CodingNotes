
# General Notes from Daily Programming

Links for Markdown documentation:
- https://www.markdownguide.org/basic-syntax/
- https://www.markdownguide.org/extended-syntax/


## Kotlin

#### 📑 Suspend function
- Part of language corutine support
- Asynchronous and non-blocking
- Can be paused and resumed

<br/>

#### 📑 Nullable Types  
Good source: https://medium.com/@fatihcoskun/kotlin-nullable-types-vs-java-optional-988c50853692

**Elvis operator :?**

```kotlin
val isOfLegalAge: Boolean = car?.driver?.age ?: 0 > 18
``` 

It means when the chain of map calls returns a non-empty age, it will be used. Otherwise the provided fallback value 0


<br/><br/>

## Spring

### Annotations

