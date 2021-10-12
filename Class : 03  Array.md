### 3.1 Topic : Array 
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
