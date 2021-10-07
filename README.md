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
### 1.7 Topic If else and Logical Operator 
use of if else :
```php
$n = 12 ;
$y = 12;
if($n == $y ){
    echo "$n is equal $y";
}else{
    echo "$n is not equal $y ";
}
//result : 12 is equal 12
```
Odd Even logic : 
```php
$n = 12 ;
if($n % 2 == 0 ){
    echo"$n is an even number";
}else{
    echo "$n is an odd number";
}
// result : 12 is an even number
```
if else Logic : 
```php
$sal = "1200";
$rahim = "343";
if ($sal == $rahim ){
    echo "$sal and $rahim are in the same position";
}elseif($sal >= $rahim){
    echo "$sal is the boss of $rahim";  
}elseif( $sal == $rahim ){
    echo "$sal is the servent of $rahim";
}
//result : 1200 is the boss of 343
echo "\n";

$age = 14;
if ($age >= 13 && $age<= 19){
    echo "He is a tineger";
}else{
    echo "He is not a tineger";
}
//result: He is a tineger
echo "\n";


$food = "salmon";
if( "tuna" == $food || "salmon" == $food ){
    echo "{$food} has vitamin D";
}elseif( "apple" == $food ){
    echo "apple doesn't conatain vitamin D ";
}else{
    echo "we dont know about this food";
}
echo "\n";
//result : salmon has vitamin D
```
Leap Year Logic : 
```php
 /* Leapyear logic :
    1. Divisible by 4 ?
    2. Divisible by 100 ?
    3. Divisible by 400 ?

 */
$year = 1900;
if ($year % 4  == 0 && $year % 100 == 0 && $year % 400 == 0){
    echo "{$year} is a leap year";
}elseif($year % 4  == 0 && $year % 100 == 0){
    echo "{$year} is not a leap year";
}elseif($year % 4  == 0){
    echo "{$year} is a leap year";
}else{
    echo "{$year} is not a leap year";
}
echo "\n";
//result : 1900 is not a leap year


if($year % 4 == 0 && ($year % 100 !== 0 || $year % 400 == 00 )){
    echo "{$year} is a leap year";
}else{
    echo "{$year} is not a leap year";
}
echo "\n";
//result : 1900 is not a leap year
```
Nested Condition : 
```php
$condtion1 = false;
$condtion2 = false;
$condtion3 = true;

if($condtion1){
    if($condtion2){
        if($condtion3){
            echo "Hello";
        }else{
            echo " Hallo 1";
        }
    }else{
        echo "Hallo 2";
    }
}else{
    echo "Hallo 3";
}
echo "\n";
if($condtion1 && $condtion2 && $condtion3){
    echo "Hello";
}elseif($condtion1 && $condtion2){
    echo " Hallo 1";
}elseif($condtion1){
    echo "Hallo 2";
}else {
    echo "Hallo 3";
}
echo "\n";
```
### 1.8 Topic : Ternary Operator
```php
$marks = 10;
if(12 == $marks){
    echo "twelve";
}elseif (10 == $marks) {
   echo "ten";
}else{
    echo"this is an unknown number";
}
echo "\n";
print ($marks == 40) ? "pass" :  "fail";

$z = 10;
$result = ($z % 2 == 0) ? "A" : (($z == 11)? "B" : "c");
echo $result;
```
### 1.9 Topic PHP Switch 
Use of Switch case :
```PHP
 $n = 12;
 $r = $n % 2;
  switch ($r){
      case 0 : 
        echo "{$n} is an even number";
        break;
    default :
    echo "{$n} is an odd number";
  }
  //result : 12 is an even number
  echo "\n";
  ```
Use of Multiple Case :
```php
$color  = "red";
switch($color){
    case "red" :
        echo "{$color} is my favorite color";
        break;
    case "green" :
        echo "{$color} is my favorite color";
        break;
    case "blue":
        echo "{$color} is not my Favorite color ";
        break;
    default :
        echo "{$color} is an unknown color";
}
//result : red is my favorite color
```
Use of ucwords() funtion and advanced Case 
```php
$color  = "green";
switch($color){
    case "red"  :
    case "green":
        echo ucwords($color)." is my favorite color";
        break;
    case "blue":
        echo "{$color} is not my Favorite color ";
        break;
    default :
        echo "{$color} is an unknown color";
}
// result : Green is my favorite color
```
Mixed Value in switch case  :
```PHP
$str = "8balls";
 switch($str){
    case (string) "9balls" :
         echo "nine balls";
        break;
    case (string) "8balls" :
        echo "Eight balls";
        break;
    default       :
        echo "No Balls";
 }
 // result : Eight balls 
 ```
 ### 1.10 PHP operator Precidence
 ```php
 $d = true || false;
 $f = false or true;
 var_dump($d, $f);
 //result : bool(true)  bool(false)

 $b = true && false ;
 $c = true and false;
 var_dump($b,$c);
 //result : bool(false)  bool(true)
 ```
### 1.11 Topic : Control Stracture Alternative Syntex :
```php
$s = 12;
if ( $s%2 == 0 ){
    echo "even Number";
}else{
    echo "Odd Number";
}
//result : even Number
echo PHP_EOL;

if ($s%2 == 0) :
    echo "even number";
else : 
    echo "odd Number";   
endif;
// Result : even number

echo PHP_EOL;
switch ( $s % 2 == 0 ) :
    case 0 :
    echo "even Number";
    break;
    default :
    echo "Odd Number";
endswitch;
//Result : Odd Number

if($s % 2 == 0) :
?>
even number 
some text 
<?php
else :
?>
odd Number 
some text++
<?php
endif;
// result : even number some text 
```

### 1.12 Determines if the argument even or odd number with function:
```php

function isEven($n) //Parameters
{ 
    if($n %2 ==0){
        return true;
    }
    return false;
}

$x=12;
if(isEven($x)){ //Arguments
   echo "$x is an Even number";
}else{
    echo "$x is an Odd number";  
}
// Result: 12 is even number
```

### 1.13 Make Factorial number with function:
```php
function factorial( int $n){
    $result=1;
    for($i= $n; $i>1; $i--){
        $result *=$i;
    }
    return $result;
}

$x=6;
echo "factorial is $x and ".factorial($x);

// result : factorial is 6 and 720
```

### 1.14 Set default parametar value with function:

```php
function serve($food="Tea",$items="2 cup"){
    
    echo "{$items} of {$food} has/have been served";
}
serve();

// result : 2 cup of tea has/have been served
```
