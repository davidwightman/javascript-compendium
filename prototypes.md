### Prototypes

prototypes are the mechanism by which JS objects inherit features from one another

**proto**

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

### Private fields

the # prevents a field from being modified

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/Private_class_fields

### static properties and methods

- only available on class and not instance

```
class Player {
	static description = "player in game"
}

Player.description
```

### extending classes

- super calls the constructor in the parent class (Player) so pass those properties in

```
class AdminPlayer extends Player {
	constructor (first, last, powers) {
		super(first, last);
		this.powers = powers;
	}
	isAdmin = true;
}

const admin = new AdminPlayer("admin", "mcadmin", ["delete", "restore world"])
```
