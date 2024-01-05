
# General Notes from Daily Programming

Links for Markdown documentation:
- https://www.markdownguide.org/basic-syntax/
- https://www.markdownguide.org/extended-syntax/


## 💜 Kotlin 💜

### ✨ Functions

#### 📑 Suspending function   
Docs: https://kotlinlang.org/docs/composing-suspending-functions.html

- Part of language corutine support
- Asynchronous and non-blocking
- Can be paused and resumed

<br/>

#### 📑 Extension function
Docs: https://kotlinlang.org/docs/extensions.html

- 

<br/>

---

<br/>

#### 📑 Map collection type
Good source: https://www.baeldung.com/kotlin/maps

- 

<br/>

#### 📑 Filtering colletctions
Docs: https://kotlinlang.org/docs/collection-filtering.html

- 

<br/>

---

<br/>

### ✨ Null safety 

#### 📑 Nullable Types  
Good source: https://medium.com/@fatihcoskun/kotlin-nullable-types-vs-java-optional-988c50853692  
Docs: https://kotlinlang.org/docs/null-safety.html#nullable-receiver

**Elvis operator *:?***

```kotlin
val isOfLegalAge: Boolean = car?.driver?.age ?: 0 > 18
``` 

It means when the chain of map calls returns a non-empty age, it will be used. Otherwise the provided fallback value 0

<br/>

**Safe calls: *let***
```kotlin
val listWithNulls: List<String?> = listOf("Kotlin", null)
for (item in listWithNulls) {
    item?.let { println(it) } // prints Kotlin and ignores null
}
```

Used to o perform a certain operation only for non-null values

<br/><br/>

## Spring

### Annotations


