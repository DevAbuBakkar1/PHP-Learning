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
### 1.3 comments 
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
```
### 1.4 Echo :
```php
$var = "shohan";
$var2 = "abu bakkar";
echo "first varible is ".$var." and second variable is ".$var2."\n";
echo "first variable is {$var} and second variable is {$var2} \n";
printf("first variable is %s and second variable is %s \n",strtoupper($var) ,$var2);
```
### 1.5  + _ * / :
```php 
$number = 12;
$number = $number +3;
echo $number;
echo "\n";

$number1 = 14;
$number1 -= 5;
echo $number1; 
echo "\n";

$number2 = 30*300;
$number3 = $number2 / (32+550);
echo $number3;

$x = $z = 5;
echo $x ."\n".$z ."\n"; // both variable's value are 5;

$x = 8;
$y = $z = $x;
echo $y."\n".$z; // both variable's value are 5;

$n = 10;
$m = $n++;
echo $m ."\n".$n;  // result 10 11

/*
$m = $n++ ;
$m = $n;
$n = $n+1;
*/
$n = 10;
$m = ++$n;
echo $m ."\n".$n;  // result 11 11

/*
$m = ++$n;
$n = $n+1; // 11
$m = $n; //11
*/

```
### 1.6 Topic :  printf() and sprintf() ; 
```php
$fName  = "abu" ;
$midName = "bakkar";
$lName = "siddiq";
//single quotation is need here
printf('His name is %1$s %2$s %3$s', $fName,$midName,$lName); 
echo "\n";
//result : his name is abu bakkar siddiq

//desimal to binarry convert;
printf('the binary equivalent of %1$d is %1$b',12);
echo "\n";
//result the binary equivalent of 12 is 1100

//show only 2numbers after . 
$num = 34.12333;
printf("%.2f",$num);
echo "\n"; 
//result 34.12

//equal all number by 000
$n = 12343;
$m = 34;
printf("%05d \n",$n);
printf("%05d \n",$m); 
/*
result :
12343 
00034
*/

$n = 1243.3433;
$m = 34.454;
printf("%07.2f \n",$n);
printf("%07.2f \n",$m); 
/*
result :
1243.34 
0034.45 
*/
$firstName = "abu";
$lastName = "bakkar";
$output = sprintf("His name is %s %s", $firstName, $lastName);//sprintf() return the valus into his variable
echo $output;
```
