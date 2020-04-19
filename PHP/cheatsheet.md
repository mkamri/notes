# PHP Cheatsheet
All the basics to set up a simple website with PHP.

## Basic Facts
* PHP runs on the web server, meaning it is **not** viewed by the actual browser.
* PHP variables always start with a `$`, both in defining them and using them.
* PHP automatically converts value types when necessary, such as converting the string `"3"` to the number `3` when necessary. This is called *type juggling*.
* You can use either single or double quotess, and if you choose double quotess you can interpolate variables (eg: `"Hello, {$name}!"`).

# Control Structures

## FOREACH
### Syntax form 1:
```
foreach (array_expression as $value) {
    statement;
}
```
Form 1 loops over the array given by `array_expression`. On each iteration, the value of the current element is assigned to `$value`. You can use `$value` in the statement as a variable.


### Syntax form 2:
```
foreach (array_expression as $key => $value) {
    statement;
}
```
Form 2 also assigns the current element's key to the `$key` variable on each iteration. 

## WHILE
### Syntax:
```
while (expr) {
    statement;
}
```
*While* tells PHP to execute the nested statements repeatedly, as long as the *while* expression evaluates to **TRUE**.\
Note that this can create an endless loop, so you must be careful that your expression will eventually evaluate to **FALSE**.\
### Example:
```
$month = 1;
while ($month <=12) {
    echo $month . ", ";
    $month = $month + 1;
}
```