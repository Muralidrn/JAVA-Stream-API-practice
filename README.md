# JAVA-Stream-API-practice

<img width="713" height="151" alt="image" src="https://github.com/user-attachments/assets/cd412c39-2c2c-45e4-bfa3-85cade768d43" />


## Examples
1. Filter Even Numbers
```
List<Integer> nums = Arrays.asList(1, 2, 3, 4, 5, 6);
List<Integer> evens = nums.stream()
    .filter(n -> n % 2 == 0)
    .collect(Collectors.toList());
System.out.println(evens);
```
```Output:
[2, 4, 6]
```
## 2. Convert Strings to Uppercase
```
List<String> names = Arrays.asList("alice", "bob", "charlie");
List<String> upper = names.stream()
    .map(String::toUpperCase)
    .collect(Collectors.toList());
System.out.println(upper);
```
```Output:
[ALICE, BOB, CHARLIE]
```
## 3. Get Word Lengths

List<String> words = Arrays.asList("java", "Stream", "api");
List<Integer> length = words.stream()
    .map(String::length)
    .collect(Collectors.toList());
System.out.println(length);
```
```Output:

text
Copy
Edit
[4, 6, 3]
```
## 4. Remove Null or Empty Strings
```java
Copy
Edit
List<String> nullStrings = Arrays.asList("hello", "", null, "world");
List<String> withoutNull = nullStrings.stream()
    .filter(n -> n != null && !n.isEmpty())
    .collect(Collectors.toList());
System.out.println(withoutNull);
```
```Output:

text
Copy
Edit
[hello, world]
```
## 5. Square and Filter Divisible by 3
```
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6);
List<Integer> squDiv = numbers.stream()
    .map(n -> n * n)
    .filter(n -> n % 3 == 0)
    .collect(Collectors.toList());
System.out.println(squDiv);
```
```Output:

text
Copy
Edit
[9, 36]
```
## 6. Extract Domain Names from Emails
java
Copy
Edit
```List<String> email = Arrays.asList("john@example.com", "alice@test.com");
List<String> domain = email.stream()
    .map(s -> s.substring(s.indexOf('@') + 1))
    .collect(Collectors.toList());
System.out.println(domain);
```
```Output:

text
Copy
Edit
[example.com, test.com]
```
## 7. Unique Words from Sentence
java
Copy
Edit
```List<String> unique = Arrays.asList("Java", "stream", "API", "is", "powerful", "and", "Java", "is", "fun")
    .stream()
    .distinct()
    .collect(Collectors.toList());
System.out.println(unique);
```
```Output:

text
Copy
Edit
[Java, stream, API, is, powerful, and, fun]
```
## 8. Count Words Greater Than 4 Characters
java
Copy
Edit
```List<String> grt4 = Arrays.asList("The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog");
long count = grt4.stream()
    .filter(word -> word.length() > 4)
    .count();
System.out.println(count);
```
```Output:

text
Copy
Edit
3
```
## 9. Capitalize First Letter of Each Word
java
Copy
Edit
```List<String> capitalize = Arrays.asList("java", "stream", "api").stream()
    .map(w -> w.substring(0, 1).toUpperCase() + w.substring(1))
    .collect(Collectors.toList());
System.out.println(capitalize);
```
```Output:

text
Copy
Edit
[Java, Stream, Api]
```
## 10. Get Words That Start with a Vowel
java
Copy
Edit
```List<String> vowelStarts = Arrays.asList("apple", "banana", "orange", "grape", "umbrella").stream()
    .filter(w -> w.matches("^[aeiouAEIOU].*"))
    .collect(Collectors.toList());
System.out.println(vowelStarts);
```
```Output:

text
Copy
Edit
[apple, orange, umbrella]
```
## 11. Keep Only Strings in Lowercase
java
Copy
Edit
```List<String> lower = Arrays.asList("Java", "python", "C++", "go").stream()
    .filter(s -> s.matches("[a-z]+"))
    .collect(Collectors.toList());
System.out.println(lower);
```
```Output:

text
Copy
Edit
[python, go]
```
## 📄 License
```This project is licensed under the MIT License.
