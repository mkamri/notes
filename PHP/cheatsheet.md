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
Note that this can create an endless loop, so you must be careful that your expression will eventually evaluate to **FALSE**.
### Example:
```
$month = 1;
while ($month <=12) {
    echo $month . ", ";
    $month = $month + 1;
}
```
Displays `1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12,`.

## IF/THEN
### Syntax:
```
if (condition) {
    statement if condition is true;
} elseif (condition2) {
    statement if condition2 is true;
} else {
    statement to run if all above are false;
}
```
Note: *elseif* and *else* are optional.

## FOR
### Syntax:
```
for (init; test; change) {
    statement to run while tesst is true;
}
```
`init` represents the innitial value. Usually `$i = 1`.\
`test` says when to stop executing the statement(s).\
`change` says how much to increment the `init` by each iteration.
### Example:
```
for ($i = 1; $i <= 10; $i++) {
    echo $i;
}
```
Displays `12345678910`.