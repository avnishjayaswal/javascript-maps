How to create a map (<a href="https://askavy.com/javascript-maps/">javascript maps</a> object)

```javascript

   var map1 = new Map([[1 , 2], [3 ,4 ] ,[5, 6]]);
   console.log(map1) ;

OUT Put
    0: {1 => 2}
    key: 1
    value: 2
    1: {3 => 4}
    key: 3
    value: 4
    2: {5 => 6}
    key: 5
    value: 6

```

```javascript

      var map2 = new Map([["firstname" ,"Avy"],  
                         ["lastname", "Jai"], 
                         ["website", "askavy"]]
                         );

        console.log(map2) ;

  out put 
  Map(3) {"firstname" => "Avy", "lastname" => "Jai", "website" => "askavy"}
  
  0: {"firstname" => "Avy"}
  1: {"lastname" => "Jai"}
  2: {"website" => "askavy"} 

```

How to use Map.set

```javascript

      var map3 = new Map();

      map3.set('key', 'value');
         
      console.log(map3) ;

OutPut
  Map(1) {"key" => "value"}
  0: {"key" => "value"}

```

How to use map.get

```javascript

      var map3 = new Map();

      map3.set('key', 'value');
         
      console.log(map3.get('key')) ;

OutPut 
Value 

```

how to use map.has

map.has return true if key found in array

```javascript
      var map3 = new Map();

      map3.set('key', 'value');
       
      console.log(map3.has('key')) ;   

OutPut
true

```

js arr map

```javascript

      var arr = [1, 2, 3, 4, 5, 6];

      var newArr = arr.map(function (val, index) {
        return { key: index, value: val };
      });

      console.log(newArr);

Output
0: {key: 0, value: 1}
1: {key: 1, value: 2}
2: {key: 2, value: 3}
3: {key: 3, value: 4}
4: {key: 4, value: 5}
5: {key: 5, value: 6}


```
javascript map array of objects

```javascript

 var arr = [
        {
          id: 1,
          name: "Avy",
        },
        {
          id: 2,
          name: "Mark",
        },
      ];

      var result = arr.map((person) => ({
        value: person.id,
        text: person.name,
      })); 

---
 result is a array that have following values
    0: {value: 1, text: "Avy"}
    1: {value: 2, text: "Mark"}

```

reformat objects javascript map array of objects

```javascript

var personsArr = [
        {
          id: 1,
          firstName: "Mark",
          lastName: "Selva",
        },
        {
          id: 2,
          firstName: "Avy",
          lastName: "Jai",
        },
        {
          id: 3,
          firstName: "Aaj",
          lastName: "kaal",
        },
      ];

      var newObj = {};

      let fullname = personsArr.map((person) => {
        newObj = person.firstName + " " + person.lastName;
        return newObj;
      });

      console.log(fullname);

OutPut
0: "Mark Selva"
1: "Avy Jai"
2: "Aaj kaal"

```

javascript map index

```javascript

          const ArrayList = ["A", "B", "C", "D", "E"];
      ArrayList.map((currentElement, index) => {
        console.log("The current iteration is: " + index + " The current element is: " + currentElement);
      });

Output
The current iteration is: 0 The current element is: A
The current iteration is: 1 The current element is: B
The current iteration is: 2 The current element is: C
The current iteration is: 3 The current element is: D
The current iteration is: 4 The current element is: E

```

javascript map reduce
The reduce() method reduces an array of values down to just one value, reducer has mainly 2 arguments first is an accumulator and second on is currentValue (currentValue is the value of array element)

there is four arguments of reduce function

accumulator – the returned value of the previous iteration
currentValue – the current item in the array
index – the index of the current item
array – the original array on which reduce was called

```javascript

           const numbers = [1, 2, 3, 4];
      const sum = numbers.reduce(function (accumulator, currentValue) {
        console.log(
          "accumulator = " + accumulator + " currentValue = " + currentValue
        );

        return accumulator + currentValue;
      }, 0);  // 0 means accumulator value is set to 0 and currentValue is 1 

Result 
accumulator = 0 currentValue = 1
accumulator = 1 currentValue = 2
accumulator = 3 currentValue = 3
accumulator = 6 currentValue = 4

```


```javascript

      const numbers = [1, 2, 3, 4];
      const sum = numbers.reduce(function (accumulator, currentValue) {
        console.log(
          "accumulator = " + accumulator + " currentValue = " + currentValue
        );

        return accumulator + currentValue;
      });  // accumulator is set 1 and  currentValue is set to 2

Result
    accumulator = 1 currentValue = 2
    accumulator = 3 currentValue = 3
    accumulator = 6 currentValue = 4

```

How to find the sum of an array of numbers

```javascript

      const numbers = [1, 2, 3, 4];
      const sum = numbers.reduce(function (accumulator, currentValue) {
        return accumulator + currentValue;
      });

      console.log(sum);  // Result 10

```

ES6 Version

```javascript

      const numbers = [1, 2, 3, 4];
      const sum = numbers.reduce((accumulator, currentValue) => {
        return accumulator + currentValue;
      });

      console.log(sum);

```

How to skip over an element in .map()

```javascript

      const numbers = [1, 2, 3, 4]; // skipping 3rd element
      const sum = numbers.reduce((accumulator, currentValue) => {
        if (currentValue == 3) {
          return false; // skip
        } else {
          return accumulator + currentValue;
        }
      });

      console.log(sum); // result 4

```

