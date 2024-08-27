# Pattern-Based Questions and Solutions 📜🎉🎈

## Q.1

```
>> *****
>> *****
>> *****
>> *****
>> *****
```

```javascript
function simplePattern1(size) {
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        for (var cols = 1; cols <= size; cols++) {
            pattern += "*";
        }
        console.log(pattern);
    }
}
```

## Q.2

```
>> *
>> **
>> ***
>> ****
>> *****
```

```javascript
function simplePattern2(size) {
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        for (var cols = 1; cols <= rows; cols++) {
            pattern += "*";
        }
        console.log(pattern);
    }
}
```

## Q.3 

```
>> *****
>> ****
>> ***
>> **
>> *
```

```javascript
function simplePattern3(size) {
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        for (var cols = 1; cols <= size - rows + 1; cols++) {
            pattern += "*";
        }
        console.log(pattern);
    }
}
```

## Q.4

```
>> 1
>> 1 2
>> 1 2 3
>> 1 2 3 4
>> 1 2 3 4 5
```

```javascript
function simplePattern4(size) {
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        for (var cols = 1; cols <= rows; cols++) {
            pattern += cols + " ";
        }
        console.log(pattern);
    }
}
```

## Q.5

```
>> *
>> **
>> ***
>> ****
>> *****
>> ****
>> ***
>> **
>> *
```

```javascript
function simplePattern5(size) {
    for (var rows = 1; rows <= size * 2 - 1; rows++) {
        var pattern = "";
        
        var con = rows <= size ? rows : 2 * size - rows;
        for (var cols = 1; cols <= con; cols++) {
            pattern += "*";
        }
        console.log(pattern);
    }
}
```

## Q.6

```
>>     *
>>    **
>>   ***
>>  ****
>> *****
```

```javascript
function simplePattern6(size) {
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for (var spaces = 1; spaces <= size - rows; spaces++) {
            pattern += " ";
        }
        
        for (var cols = 1; cols <= rows; cols++) {
            pattern += "*";
        }
        console.log(pattern);
    }
}
```

## Q.7

```
>> *****
>>  ****
>>   ***
>>    **
>>     *
```

```javascript
function simplePattern7(size) {
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for (var spaces = 1; spaces <= rows - 1; spaces++) {
            pattern += " ";
        }
        
        for (var cols = 1; cols <= size - rows + 1; cols++) {
            pattern += "*";
        }
        console.log(pattern);
    }
}
```

## Q.8

```
>>     *
>>    ***
>>   *****
>>  *******
>> *********
```

```javascript
function simplePattern8(size) {
    var temp = 1;
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for (var spaces = 1; spaces <= size - rows; spaces++) {
            pattern += " ";
        }
        
        for (var cols = 1; cols <= temp; cols++) {
            pattern += "*";
        }
        temp = temp + 2;
        console.log(pattern);
    }
}
```

## Q.9

```
>> *********
>>  *******
>>   *****
>>    ***
>>     *
```

```javascript
function simplePattern9(size) {
    var temp = size * 2 - 1;
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for (var spaces = 1; spaces <= rows; spaces++) {
            pattern += " ";
        }
        
        for (var cols = 1; cols <= temp; cols++) {
            pattern += "*";
        }
        temp = temp - 2;
        console.log(pattern);
    }
}
```

## Q.10

```
>>     *
>>    * *
>>   * * *
>>  * * * *
>> * * * * *
```

```javascript
function simplePattern10(size) {
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for (var spaces = 1; spaces <= size - rows; spaces++) {
            pattern += " ";
        }
        
        for (var cols = 1; cols <= rows; cols++) {
            pattern += "* ";
        }
        console.log(pattern);
    }
}
```

## Q.11

```
>> * * * * *
>>  * * * *
>>   * * *
>>    * *
>>     *
```

```javascript
function simplePattern11(size) {
    for (var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for (var spaces = 1; spaces <= rows; spaces++) {
            pattern += " ";
        }
        
        for (var cols = 1; cols <= size - rows + 1; cols++) {
            pattern += "* ";
        }
        console.log(pattern);
    }
}
```

## Q.12

```
>> * * * * *
>>  * * * *
>>   * * *
>>    * *
>>     *
>>     *
>>    * *
>>   * * *
>>  * * * *
>> * * * * *
```

```javascript
function simplePattern12(size) {
    for (var rows = 1; rows <= size * 2; rows++) {
        var pattern = "";
        
        var spaceCon = rows <= size ? rows - 1 : size - (rows - size);
        for (var spaces = 1; spaces <= spaceCon; spaces++) {
            pattern += " ";
        }
        
        var con = rows <= size ? size - rows + 1 : rows - size;
        for (var cols = 1; cols <= con; cols++) {
            pattern += "* ";
        }
        console.log(pattern);
    }
}
```

## Q.13

```
>>     *
>>    * *
>>   *   *
>>  *     *
>> *********
```

```javascript
function simplePattern13(size) {
    var temp = 1;
    for(var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for(var spaces = 1; spaces <= size - rows; spaces++) {
            pattern += " ";
        }
        
        for(var cols = 1; cols <= temp; cols++) {
            if(rows === size) {
              pattern += "*";   
            } else if(cols === 1 || cols === temp) {
                pattern += "*";   
            } else {
                pattern += " ";
            }
        }
        temp += 2
        console.log(pattern);
    }
}
```

## Q.14

```
>> *********
>>  *     *
>>   *   *
>>    * *
>>     *
```

```javascript
function simplePattern14(size) {
    var temp = size * 2 - 1;
    for(var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for(var spaces = 1; spaces <= rows - 1; spaces++) {
            pattern += " ";
        }
        
        for(var cols = 1; cols <= temp; cols++) {
            if(rows === 1) {
              pattern += "*";   
            } else if(cols === 1 || cols === temp) {
                pattern += "*";   
            } else {
                pattern += " ";
            }
        }
        temp -= 2
        console.log(pattern);
    }
}
```

## Q.15

```
>>     *
>>    * *
>>   *   *
>>  *     *
>> *       *
>>  *     *
>>   *   *
>>    * *
>>     *
```

```javascript
function simplePattern15(size) {
    var temp = 1;
    for(var rows = 1; rows <= size * 2 - 1; rows++) {
        var pattern = "";
        
        var spaceCon = rows <= size ? size - rows : rows - size;
        for(var spaces = 1; spaces <= spaceCon; spaces++) {
            pattern += " ";
        }
        
        for(var cols = 1; cols <= temp; cols++) {
            if(cols === 1 || cols === temp) {
                pattern += "*";   
            } else {
                pattern += " ";
            }
        }
        temp = rows < size ? temp + 2 : temp - 2;

        console.log(pattern);
    }
}
```

## Q.16

```
>>         1
>>       1   1
>>     1   2   1
>>   1   3   3   1
>> 1   4   6   4   1
```

```javascript
function simplePattern16(size) {
    for(var rows = 1; rows <= size ; rows++) {
        var pattern = "";
        
        for(var spaces = 1; spaces <= size - rows; spaces++) {
            pattern += " ";
        }
        
        var value = 1;
        for(var cols = 1; cols <= rows; cols++) {
            pattern += value + "  ";
            value = value * (rows - cols) / cols
        }
        console.log(pattern);
    }
}
```

## Q.17

```
>>    1
>>   212
>>  32123
>> 4321234
>>  32123
>>   212
>>    1
```

```javascript
function simplePattern17(size) {
    for(var rows = 1; rows <= size * 2 - 1 ; rows++) {
        var pattern = "";
        var con = rows <= size ? rows: size * 2 - rows;
        var spaceCon = rows <= size ? size - rows : rows - size;
        for(var spaces = 1; spaces <= spaceCon; spaces++) {
            pattern += " ";
        }
        
        for(var cols = con; cols >= 1; cols--) {
            pattern += cols;
        }
        
        for(var cols = 2; cols <= con; cols++) {
            pattern += cols;
        }
        
        console.log(pattern);
    }
}
```

## Q.18

```
>> **********
>> ****  ****
>> ***    ***
>> **      **
>> *        *
>> *        *
>> **      **
>> ***    ***
>> ****  ****
>> **********
```

```javascript
function simplePattern18(size) {
    var step = 0;
    for(var rows = 1; rows <= size * 2 ; rows++) {
        var pattern = "";
        
        var con = rows <= size ? size - rows + 1 : rows - size ;
        for(var cols = 1; cols <= con; cols++) {
            pattern += "*";
        }
        
        for(var spaces = 1; spaces <= step; spaces++) {
            pattern += " ";
        }

        if(rows===size) {
            step = 10;
        }
        step = rows < size ? step + 2: step - 2;
        
        for(var cols = 1; cols <= con; cols++) {
            pattern += "*";
        }
        
        console.log(pattern);
    }
}
```

## Q.19

```
>> *        *
>> **      **
>> ***    ***
>> ****  ****
>> **********
>> ****  ****
>> ***    ***
>> **      **
>> *        *
```

```javascript
function simplePattern19(size) {
    var step = 2 * size - 2;
    for(var rows = 1; rows <= size * 2 - 1 ; rows++) {
        var pattern = "";
        
        var con = rows <= size ? rows : size * 2 - rows ;
        for(var cols = 1; cols <= con; cols++) {
            pattern += "*";
        }
        
        for(var spaces = 1; spaces <= step; spaces++) {
            pattern += " ";
        }

        step = rows < size ? step - 2: step + 2;
        
        for(var cols = 1; cols <= con; cols++) {
            pattern += "*";
        }
        
        console.log(pattern);
    }
}
```

## Q.20

```
>> ****
>> *  *
>> *  *
>> *  *
>> ****
```

```javascript
function simplePattern20(size) {
    for(var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for(var cols = 1; cols <= size - 1; cols++) {
            if(rows === 1 || rows === size) {
                pattern += "*";   
            } else if(cols === 1 || cols === size - 1) {
                pattern += "*";   
            } else {
                pattern += " ";
            }
        }
        
        console.log(pattern);
    }
}
```

## Q.21

```
>> 1
>> 2  3
>> 4  5  6
>> 7  8  9  10
>> 11 12 13 14 15
```

```javascript
function simplePattern21(size) {
    var counter = 1;
    for(var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        for(var cols = 1; cols <= rows; cols++) {
            pattern += counter + " ";
            counter += 1;
        }
        
        console.log(pattern);
    }
}
```

## Q.22

```
>> 1
>> 0 1
>> 1 0 1
>> 0 1 0 1
>> 1 0 1 0 1
```

```javascript
function simplePattern22(size) {
    for(var rows = 1; rows <= size; rows++) {
        var pattern = "";
        
        value = 1;
        for(var cols = 1; cols <= rows; cols++) {
            value = (1 + rows + cols) % 2 === 0 ? 0 : 1;
            pattern += value + " ";
        }
        
        console.log(pattern);
    }
}
```