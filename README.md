# PHP-Learning
### 1. variable  : 
Variable output ways :
```PHP
 //First Way .
 $var = "Name is";
 $var_1 = "AbU Bakkar";
 
 echo "Who are you?";
 echo 'My'.$var"".$var_1; //this is not standerd way 
 
 //second way : you must write in double qoutation "" .and this is standerd way 
 echo "my {$var}, {var_1}";
 
//to separate onle line to another we can use :here we must use double quotation .
echo  "\n"; 
```


### 1.2 variable : 
Variable output ways : constant variable will be in capital letter so that it can easily identified as constant

```PHP
define ('PI', 'Hy Abu Bakkar');
echo PI  //or echo "my name is ".PI;

//change the variable value ;
$var = "this is shohan";
echo $var;
$var = "this is abu Bakkar";
echo $var;
```
### 2.comments 
Single and multiple comment syntex
```PHP
// This is single line comment 
# this is also single line comment
/*
multiple line comment
line one 
line two
line three
and more .......
*/

