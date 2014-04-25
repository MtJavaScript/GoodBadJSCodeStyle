Good and bad JavaScript code style
==================

Preface
--------------------------------------
 What for to write good code  
 1. Less time to understand, fix, extend
 2. Less time means less money to do project.
 3. Less bugs
 4. Flexibility, extesibility, comfortability, readability
 5. Good mood when work with good code
 6. Increase level of team
 7. Increase cost of project by flexibility and exensibility
 8. Elegant code

Let's start
--------------------------------------

###1 - if/for without brackets
Everybody who learn in University is studied by C/C++ and learned to write.
Many old C/C++ books are full of such code.  
```javascript
//Bad
if(n)
   a = 5;
```
This gives  
1. More bugs easy to do
   If to do new line, which is almost always needed and forget to add brackets than bugs  
   that you would search much time.  
2. More time to support and keep in mind do not do bug with new line  
3. A bit decrease readability of code in about 30-50%.  

So write this
```javascript
//Good
if(n){
  a = 5;
}
```
More bad code in this style
```javascript
//Bad
for (key in source)
      if (source[key] !== undefined)
        target[key] = source[key]
```

###2 - where to put spaces
Spaces also can do code or easy or complex

```javascript
//Bad
if (n) {
   a = 5;
}
```

```javascript
//Good
if(n){
   a = 5;
}
```
  
```javascript
//Bad
var o = {
   load:function() {
      
   }
};
```

```javascript
//Good
var o = {
   load: function(){
      
   }
};
```

### 3 - ?: - ternary operator
Try to avoid this operator.  
When developers starts to code they learn this operator and them get habbit to write it instead of if.  
Use ternary operator when there is no way to write over if.  
  
ternary operator does code more complex.

### 4 - if with equation
```javascript
//Bad
if( a = b = this.getName()){

}
```

```javascript
//Good
a = this.getName();
b = a;
if(a){

}
```

Equation in if does code more complex

### 5 - Many vars

```javascript
//Bad
var a = 5;
var b = 7;
var c = 10;
```

```javascript
//Good
var a = 5,
    b = 7,
    c = 10;
```

Many vars decrease a bit readability of code.  
And does code less elegant.

### 6 - Array on several rows. Style to avoid extra comma.
```javascript
//Bad
var arr = [
   {
      a: 5,
      b: 10
   }
   ,
   {
      a: 10, b: 12
   }
   ];
```

```javascript
//Good
var arr = [{
   a: 5,
   b: 10
},{
   a: 10,
   b: 12
}];
```
There are many repos, especially on node.js with that bad code style.  
This does code not elegant, and copmlex to read.  

### 7 - new line

```javascript
//Bad
function a(){
  var a = 5;
  console.log(a);
  return a + 5;
}
```
  

```javascript
//Good
function a(){
  var a = 5;
  
  console.log(a);
  
  return a + 5;
}
```

It is needed to do new line after var declaring and before return.  
