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
### 3.06 Topic : Copy by Value Copy by reference 
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
