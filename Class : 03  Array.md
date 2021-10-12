### 3.01 Topic : Array 
```php
$students = array(
    "rahim",
    "jahid",
    123,
    "moinr"
);

# output data :
//var_dump($students);
//print_r($students);

//output data with for loop
$c = count($students);
for($i = 0; $i<$c; $i++ ){
    echo $students[$i] ."\n";
}
//reverse data with for loop 
for($i = $c-1 ; $i>= 0; $i--){
    echo $students[$i]."\n";
}
```

### 3.02  Topic: Array Manupulation :-
```php

to entry the value into an array:
array_unshift(); //add element in the last of array; 
array_push();//add element in the last of array; 

$boys = array(
    "robi",
    'tuhin',
    'jamal',
    335,
);

//to change the old data with new :
$boys[3] = "marjan"; //335 will be changed with marjan

array_unshift($boys , "first boy"); //add value in first 
array_unshift($boys , "first boy 2"); //add value in first 
array_push($boys, "last boy"); //add value in last
$boys[] ="last boy"; //add value in last 

/*
to bring out the value from an array:
array_pop(); //last element of array will be remove and returen 
array_shift();//first element of array will be remove and returen 
*/
array_pop($boys);//last value has removed 
array_shift($boys); //first value has removed 


$count_boys = count($boys);
for($i = 0; $i < $count_boys; $i++){
    echo $boys[$i] ."\n";
}
```
### 3.03 Topic : associative array :-
```php
$foods  = array(
    "vagitable" => 'brinjal,brocolli,carrot,capsicam',
    "fruits" => 'orange,mango,lichi,apple',
    'drinks' => 'water, milk, pepsi',
);
//simple output :
echo $foods['vagitable'];
//result : brinjal,brocolli,carrot,capsicam

//output with foreach loop :
echo PHP_EOL;
foreach($foods as $keys => $value){
    echo $keys . " = " .$value."\n";
}
//outpur with print_r() array_keys() and array_values()
$keys = array_keys($foods);
print_r($keys);

//output with for loop 
echo PHP_EOL;
$keys = array_keys($foods);
for($i =0; $i<count($keys); $i++){
    $key = $keys[$i];
    echo $foods[$key]."\n";
}
echo PHP_EOL;
$values = array_values($foods);
for($i =0; $i<count($values); $i++){
    $value = $values[$i];
    echo $value ."\n";  
}
```
### 3.04 Topic :String to array, array to string and multiple delimeter 
```php
//String to array
$vagitable = explode(',','brinjal,brocolli,carrot,capsicam');

//multiple delimeter : 
$vagitable = preg_split('/(, |,)/','brinjal,brocolli,carrot,capsicam');
print_r($vagitable);

#var_dump($vagitable);
echo $vagitable[0];

echo PHP_EOL;
//array to string
$arryToString = join(', ', $vagitable);
echo $arryToString;
```
### 3.05 Topic : Multidimentional Array or Nested Array :
```php
$foods= [
    'vagitable' => explode(',','brinjal,brocolli,carrot,capsicam'),
    "fruits" => explode(',','orange,mango,lichi,apple'),
    'drinks' => explode(',','water, milk, pepsi'),
];
print_r($foods);

//to add value in array
array_push($foods['drinks'],'orange juice','ginger');
print_r($foods);
$newarray= [
    [
        [
            [
                ['shohan']
            ],
        ],
    ],
];
var_dump($newarray);
echo $newarray[0][0][0][0][0];
```
### 3.06 Topic : Associative array 
```php
$student = array(
    'fname' => 'jamal',
    'lname' => 'ahmed',
    'age' => '21',
    'class' => 12,
    'section' => 'humanity'
);
print_r($student);
echo $student['fname']."\n".$student['lname']."\n";
printf("%s %s \n", $student['age'],$student['section']);

$serialized = serialize($student);
echo $serialized ;
echo PHP_EOL;

$unSerialized = unserialize($serialized);
print_r($unSerialized);
echo "\n";

$jsonData = json_encode($student);
echo $jsonData;
echo "\n";

$jsonDatadecode = json_decode($jsonData, true);
print_r($jsonDatadecode);
echo "\n";
```
### 3.07 Topic : Copy by Value Copy by reference 
```php
$person = array('fname' => 'hellow', 'lname' => 'world');
$newperson = $person ;
$newperson ['lname'] ='shohan';
print_r($person);
print_r($newperson);

function printdata($person){
    $person['lname'] .= " changed";
    print_r($person);
}
printdata($person);
print_r($person);
```

### 3.08 Topic : Empty Value Check 
```php
$name = '';
//check is variable set or not 
if(isset($name)){
    echo "name variable is set";
}else{
    echo "name variable is not set";
}
//result : name is set

echo PHP_EOL;
$name = 0;
//check variable empty or not 
if(empty($name)){
    echo "name is empty";
}else {
    echo "His Name is {$name}";
} // result : name is empty
//this is problem Solution is :

echo "\n";
$name = 0;
if(isset($name) && (is_numeric($name) || $name != '')){
    echo "name is set and his name is {$name}";
}else{
    echo "name is not set and value is empty";
}
//result : name is set and his name is 0
```
### 3.09 Topic : Array Slice
```php
//example or array
$fruits = array('apple','banana','mango','lichi','dates','palm','orange');
$somefruits = array_slice($fruits,2); //start from 2
$somefruits = array_slice($fruits,2,3); // start from 2 and end afeter 3
$somefruits = array_slice($fruits,2,-1); //start from 2 and end before last 
$somefruits = array_slice($fruits,-5,-1);// start from -5 and end before last 
$somefruits = array_slice($fruits,2,-1,true); //start from 2 and end before last also maintin serializie
print_r($somefruits);
/* result :
Array
(
    [0] => mango
    [1] => lichi
    [2] => dates
)
*/

//example of associative array : 
$anotherfruits = array('a'=>'apple','b'=>'banana', "kola", 23=>34, 'c'=>'mango','d'=>'lichi','e'=>'dates','f'=>'palm','g'=>'orange');
$randfruits = array_slice($anotherfruits,2, -1, true);
print_r($randfruits);
/* result :
Array
(
    [0] => kola
    [23] => 34
    [c] => mango
    [d] => lichi
    [e] => dates
    [f] => palm
)
*/
```
### 3.10 Topic : Array_splice
```php
$fruits = array('apple','banana','mango','lichi','dates','palm','orange');
//separate value from array completely 
 $splice = array_splice($fruits , 2 , -1);
 //separate date from value and entry data in the same position
 $newdata = array('jackfruit', 'tamarind', 'pineapple');
 $splice = array_splice( $fruits , 2 , -1, $newdata);
 print_r($splice);
 print_r($fruits);
 /*result :
 Array
(
    [0] => mango
    [1] => lichi
    [2] => dates
    [3] => palm
)
Array
(
    [0] => apple
    [1] => banana
    [2] => jackfruit
    [3] => tamarind
    [4] => pineapple
    [5] => orange
)
*/
```
### 3.09 Topic : Array_merge
```php 
$fruits = array('apple','banana','mango','lichi','dates','palm','orange');
$fruts1 = array_slice($fruits, 1, 3);
$fruts2 = array_slice($fruits, 4, null ,true);//true is for sencond output 

// output way 01 :
$newfruits = array_merge($fruts1,$fruts2);
print_r($fruts1);
print_r($fruts2);
print_r($newfruits);

// output way 02 :
$newfruitsplus = $fruts1 + $fruts2;
print_r($newfruitsplus);


//associative array marge :
$anotherfruits = array('a'=>'apple','b'=>'banana', "kola", 23=>34, 'c'=>'mango','d'=>'lichi','e'=>'dates','f'=>'palm','g'=>'orange');
/*this way is not work properly
$splice_fruit= array_splice($anotherfruits, 2, 2 , array('j' =>"komla", 4 =>5));
print_r($splice_fruit);
print_r($anotherfruits);
*/
$fruit1 = array_slice($anotherfruits , 0 ,3 ,true);
$fruts2 = array_slice($anotherfruits , 4 , null , true);
$fruit3 = array( "new" => "komla", 342=> 3454);
$final_marge = $fruit1 + $fruts2 + $fruit3 ;

print_r($final_marge);
/*
Result :
Array
(
    [a] => apple
    [b] => banana
    [0] => kola
    [c] => mango
    [d] => lichi
    [e] => dates
    [f] => palm
    [g] => orange
    [new] => komla
    [342] => 3454
)
*/
```
