# PHP Cheatsheet
All the basics to set up a simple website with PHP.

## Basic Facts
* PHP runs on the web server, meaning it is **not** viewed by the actual browser.
* PHP variables always start with a `$`, both in defining them and using them.
* PHP automatically converts value types when necessary, such as converting the string `"3"` to the number `3` when necessary. This is called *type juggling*.
* You can use either single or double quotess, and if you choose double quotess you can interpolate variables (eg: `"Hello, {$name}!"`).

# Control Structures

## foreach
Syntax: 
```
foreach (array_expression as $value) {
    statement;
}
```
OR
```
foreach (array_expression as $key => $value) {
    statement
}
```
