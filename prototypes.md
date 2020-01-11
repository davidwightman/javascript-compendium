### Prototypes

prototypes are the mechanism by which JS objects inherit features from one another

__proto__

### factory functions

### Constructor functions and the new 

new keyword does the following things:
Creates a blank, plain JavaScript object;
Links (sets the constructor of) this object to another object;
Passes the newly created object from Step 1 as the this context;
Returns this if the function doesn't return its own object.

methods should be called outside:
```
function Color(r,g) {
    this.r = r;
    this.g = g;
}
Color.prototype.rgb = function() {}
```

### Classes

define class with class keyword
capitalize name
add constructor - will run automatically when instantiated a new instance
methods in class are added to the prototype

```
class Color {
    constructor(r, g, b) {
        this.r = r;
        this.g = g;
        this.b = b;
    }
    rgb() {
        return `hi ${this.b}`
    }
}
const dave = new Color(2, 3, 4)
```

### extends and super

dog does not add any new properties and does not need constructor
cat does add livesLeft so you need the constructor with super and pass in name and age to take advantage of Pet constructor

```
class Pet {
	constructor(name, age) {
		console.log('IN PET CONSTRUCTOR!');
		this.name = name;
		this.age = age;
	}
	eat() {
		return `${this.name} is eating!`;
	}
}

class Cat extends Pet {
	constructor(name, age, livesLeft = 9) {
		console.log('IN CAT CONSTRUCTOR!');
		super(name, age);
		this.livesLeft = livesLeft;
	}
	meow() {
		return 'MEOWWWW!!';
	}
}

class Dog extends Pet {
	bark() {
		return 'WOOOF!!';
	}
	eat() {
		return `${this.name} scarfs his food!`;
	}
}

```