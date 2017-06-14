<p align="center">
<img alt="Kotlin" height="200" width="200" src="http://antonioleiva.com/wp-content/uploads/2015/03/kotlin.png">
<img alt="Swift" height="200" width="300" src="https://cdn1.macworld.co.uk/cmsdata/features/3523633/swift_3_thumb800.jpg">
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

```java
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

```objective-c
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

```objective-c
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

```objective-c
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

```objective-c
NSDictionary *dic = @{@"key1":@"value1", @"key2":@"value2"};

[dic objectForKey:@"key1"];

// traversing
for (NSString* key in dic) {
  NSLog(@"%@", [dic objectForKey:key]);
}

```

---
### For loop
> Java

```java
for (int i = 1; i <= 10 ; i++) { }
for (int i = 1; i < 10 ; i++) { }
for (int i = 10; i >= 1 ; i--) { }
for (int i = 1; i <= 10 ; i+=2) { }
for (int i = 10; i >= 1 ; i-=2) { }
for (String item : collection) { }
for (Map.Entry<String, String> entry: map.entrySet()) { }

for (Car car : cars) {}
```

> Kotlin

```kotlin
for (i in 1..10) { }
for (i in 1 until 10) { }
for (i in 10 downTo 1) { }
for (i in 1..10 step 2) { }
for (i in 10 downTo 1 step 2) { }
for (item in collection) { }
for ((key, value) in map) { }

cars.forEach {  }
```

> Swift

```swift
for i in 1...10 {}
for i in 1..<10 {}
for i in stride(from: 10, to: 1, by: -1) {} or for i in (1...10).reversed() {}
for i in stride(from: 1, to: 10, by: 2) {}
for i in stride(from: 10, to: 1, by: -2) {}
for item in collection {}
for (k,v) in dic {}

cars.forEach { (item) in 
  // 
}
```

> Objective C
```objective-c
for (int i = 1; i <= 10 ; i++) { }
for (int i = 1; i < 10 ; i++) { }
for (int i = 10; i >= 1 ; i--) { }
for (int i = 1; i <= 10 ; i+=2) { }
for (int i = 10; i >= 1 ; i-=2) { }
for (id item in collection) {}
for (NSString* key in dic) { }

for (Car *car in cars) {}
```

---
### Instance check
> Java

```java
int score = // some score;
String grade;
switch (score) {
	case 10:
	case 9:
		grade = "Excellent";
		break;
	case 8:
	case 7:
	case 6:
		grade = "Good";
		break;
	case 5:
	case 4:
		grade = "Ok";
		break;
	case 3:
	case 2:
	case 1:
		grade = "Fail";
		break;
	default:
	    grade = "Fail";				
}
```

> Kotlin

```kotlin
var score = // some score
var grade = when (score) {
	9, 10 -> "Excellent" 
	in 6..8 -> "Good"
	4, 5 -> "Ok"
	in 1..3 -> "Fail"
	else -> "Fail"
}
```

> Swift

```swift
let score = 1
var grade = String()
switch score {
  case 9, 10:
     grade = "Good"
  case 6...8:
     grade = "Good"
  case 4,5:
     grade = "Ok"
  case 1...3:
     grade = "Fail"
  default:
     grade = "Fail"
}
```

> Objective C
```objective-c
NSInteger score = 9;
NSString *grade = [[NSString alloc] init];
switch (score) {
  case 9:
  case 10:
    grade = @"Excellent";
    break;
  case 6:
  case 7:
  case 8:
    grade = @"Good";
    break;
  case 4:
  case 5:
    grade = @"Ok";
    break;
  case 1:
  case 2:
  case 3:
    grade = @"Fail";
    break;   
  default:
    grade = @"Fail";
    break;
}
```

---
### Filtering a list
> Java

```java
final List<Integer> list = Arrays.asList(1, 2, 3, 4);
for (Integer i : list) {
  if (i % 2 == 0) {
     System.out.println(i);
  }
}
```

> Kotlin

```kotlin
val list = listOf(1, 2, 3, 4)
list.filter { it % 2 == 0 }
    .forEach { print(it) }
```

> Swift

```swift
let list = [1, 2, 3, 4]
list.filter({$0 % 2 == 0})
    .forEach({print("\($0)")})
```

> Objective C
```objective-c
NSArray *array = [[NSArray alloc] initWithObjects:@1, @2, @3, @4, nil];
for (id item in array) {
  if ([item integerValue] % 2 == 0) {
     NSLog(@"%@", item);
  }
}
```

---
### Ternary operator
> Java

```java
String result = //
String message = result != null ? result : "Empty result";
```

> Kotlin

```kotlin
var result = //
var message = result ?: "Empty result"
```

> Swift

```swift
var result: String?
let message = result != nil ? result! : "Empty result"
```
> Objective C

```objective-c
NSString *result;
NSString *message = result ? result : @"Empty result";
```

---

Updating...

