# TASKS_KOTLIN_INTRODUCTION
Task № 1
Simple Functions
Check out the function syntax and change the code to make the function start return the string "OK".
In the Kotlin Koans tasks, the function TODO() will throw an exception. To complete Kotlin Koans, you need to replace this function invocation with meaningful code according to the problem.

Task № 2
Named arguments
Make the function joinOptions() return the list in a JSON format (for example, [a, b, c]) by specifying only two arguments.
Default and named arguments help to minimize the number of overloads and improve the readability of the function invocation. The library function joinToString is declared with default values for parameters:
fun joinToString(
    separator: String = ", ",
    prefix: String = "",
    postfix: String = "",
    /* ... */
): String
It can be called on a collection of Strings.

Task № 3
Default arguments
Imagine you have several overloads of 'foo()' in Java:
public String foo(String name, int number, boolean toUpperCase) {
    return (toUpperCase ? name.toUpperCase() : name) + number;
}
public String foo(String name, int number) {
    return foo(name, number, false);
}
public String foo(String name, boolean toUpperCase) {
    return foo(name, 42, toUpperCase);
}
public String foo(String name) {
    return foo(name, 42);
}
You can replace all these Java overloads with one function in Kotlin. Change the declaration of the foo function in a way that makes the code using foo compile. Use default and named arguments.

Task № 4
Triple-quoted strings
Learn about the different string literals and string templates in Kotlin.
You can use the handy library functions trimIndent and trimMargin to format multiline triple-quoted strings in accordance with the surrounding code.
Replace the trimIndent call with the trimMargin call taking # as the prefix value so that the resulting string doesn't contain the prefix character.

Task № 5
String templates
Triple-quoted strings are not only useful for multiline strings but also for creating regex patterns as you don't need to escape a backslash with a backslash.
The following pattern matches a date in the format 13.06.1992 (two digits, a dot, two digits, a dot, four digits):
fun getPattern() = """\d{2}\.\d{2}\.\d{4}"""
Using the month variable, rewrite this pattern in such a way that it matches the date in the format 13 JUN 1992 (two digits, one whitespace, a month abbreviation, one whitespace, four digits).

Task № 6
Nullable types
Learn about null safety and safe calls in Kotlin and rewrite the following Java code so that it only has one if expression:
public void sendMessageToClient(
    @Nullable Client client,
    @Nullable String message,
    @NotNull Mailer mailer
) {
    if (client == null || message == null) return;
​
    PersonalInfo personalInfo = client.getPersonalInfo();
    if (personalInfo == null) return;
​
    String email = personalInfo.getEmail();
    if (email == null) return;
​
    mailer.sendMessage(email, message);
}

Task № 7
Nothing type
Nothing type can be used as a return type for a function that always throws an exception. When you call such a function, the compiler uses the information that the execution doesn't continue beyond the function.
Specify Nothing return type for the failWithWrongAge function. Note that without the Nothing type, the checkAge function doesn't compile because the compiler assumes the age can be null.

Task № 8
Lambdas
Kotlin supports functional programming. Learn about lambdas in Kotlin.
Pass a lambda to the any function to check if the collection contains an even number. The any function gets a predicate as an argument and returns true if at least one element satisfies the predicate.
