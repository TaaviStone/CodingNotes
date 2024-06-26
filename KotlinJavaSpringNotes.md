# General Notes from Daily Programming at work

Links for Markdown documentation:
- https://www.markdownguide.org/basic-syntax/
- https://www.markdownguide.org/extended-syntax/


## 💜 Kotlin 💜

See variable type - *Ctrl + Shift + P*  
Val quick docs - *Ctrl + Q*

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


#### 📑 runBlocking

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
Docs: https://kotlinlang.org/docs/null-safety.html

**Not-null assertion operator  *!!***  
Converts any value to non-nullable type and throws an exeption if the value is null.

**Safe call operator  *?.***  
Returns ```null``` if value itself is null. Good to use in chains

<br/>

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

**Either**

<br/><br/>

### ✨ Miscellaneous

#### Singelton method  
Good source: https://www.geeksforgeeks.org/singleton-class-java/

#### either {} & .bind


#### Small either and big Either


companion object

## Spring

### Annotations

@Generated
