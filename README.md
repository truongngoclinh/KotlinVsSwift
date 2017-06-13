<p align="center">
<img alt="Kotlin" height="200" width="200" src="http://antonioleiva.com/wp-content/uploads/2015/03/kotlin.png">
<img alt="Swift" height="200" width="300" src="https://cdn1.macworld.co.uk/cmsdata/features/3523633/swift_3_thumb800.jpg">
</p>


</p>


# Kotlin vs Swift 3 

> Kotlin is Swift in Android? - How they look!

> I added Java & Objective C syntax also, so everyone can easily understand the code.

> Reference to [`Mindorks: from Java to Kotlin`](https://github.com/MindorksOpenSource/from-java-to-kotlin)

--- 
### Variable, Constant declaration
> Java

```java
String name = "Linh Truong";
final String name = "Linh Truong";
```

> Kotlin

```kotlin
var name = "Linh Truong"
var name: String = "Linh Truong"
val name = "Linh Truong"
```

> Swift

```swift
var name = "Linh Truong"
var name: String = "Linh Truong"
let name = "Linh Truong"
```
> Objective C

```c
NSString *name = @"Linh Truong";
static NSString *const name = @"Linh Truong";
```
---
### Display text
> Java

```java
System.out.print("Linh Truong");
System.out.println("Linh Truong");

String firstName = "Linh";
String lastName = "Truong";
String message = "My name is: " + firstName + lastName;
```

> Kotlin

```kotlin
print("Linh Truong")
println("Linh Truong")

var firstName = "Linh"
var lastName = "Truong"
var message = "My name is: $firstName $lastName" 
```

> Swift

```swift
print("Linh Truong)
print("\nLinh Truong")

var firstName = "Linh"
var lastName = "Truong"
var message = "My name is: \(firstName) \(lastName)"
```
> Objective C

```c
NSLog("Linh Truong");
NSLog("\nLinh Truong");

NSString *firstName = @"Linh";
NSString *lastName = @"Truong";
NSString *message = [NSString stringWithFormat:@"My name is: %@ %@", firstName, lastName];
```

---
### Optional or null (nil) case
> Java

```java
String name;
name = null;

if (name != null) {
  // excute if not null
}
```

> Kotlin

```kotlin
var name: String?
name = null

name?.let {
   // excute if not null
}
```

> Swift

```swift
var name: String?
name = nil

if let not_null_name = name {
  // excute if not null
}
```
> Objective C

```c
NSString *name = @"Linh Truong";
name = nil;

if (name) {
  // excute if not null
}
```

---
### Declare a function
> Java

```java
void display(String firstName, String lastName) {}
int add(int x, int y) {}

display("Linh", "Truong");
```

> Kotlin

```kotlin
fun display(firstName: String, lastName: String) {}
fun display(firstName: String = "defaultFirstName", lastName: String = "defaultLastName") {}
fun add(x: Int, y: Int): Int {}

display("Linh", "Truong")
```

> Swift

```swift
func display(firstName: String, lastName: String) {}
display(firstName: "Linh", lastName: "Truong")

func display(_ firstName: String, _ lastName: String) {}
display("Linh", "Truong")

func add(x: Int, y: Int) -> Int {}
```

> Objective C

```c
- (void)display:(NSString*)firstName :(NSString*)lastName {}
[self display:@"Linh" :@"Truong"];
 
- (void)displayWithFirstName:(NSString*)first LastName:(NSString*)last {}
[self displayWithFirstName:@"Linh" LastName:@"Truong"];;

- (int)add:(int)x :(int)y {}
```

---
### Map or Dictionary
> Java

```java
Map<String, String> map = new HashMap<>();
map.add("key1", "value1");
map.add("key2", "value2");

map.get("key1")

// traversing
for (Map.Entry<String, String> entry : map.entrySet()) {
  System.out.print(entry.getKey() + " -> " + entry.getValue());
}
```

> Kotlin

```kotlin
var map = mapOf("key1" to "value1", "key2" to "value2")

map["key1"]

// traversing
for ((k, v) in map) {
  print("$k -> $v");
}
```

> Swift

```swift
var dic: [String: String] = ["key1":"value1", "key2":"value2"]

dic["key1"]

// traversing
for (key, value) in dic {
  print("\(key) -> \(value)")
}
```

> Objective C

```
NSDictionary *dic = @{@"key1":@"value1", @"key2":@"value2"};

[dic objectForKey:@"key1"];

// traversing
for (NSString* key in dic) {
  NSLog(@"%@", [dic objectForKey:key]);
}

```

---

Updating...

