### Numbers and BigInts

numbers with limited precision

# special types

Nan - typeof(NaN) // 'number'. result of 0/0
Infinity
-Infinity
-0

# special functions we can use with numbers

const num = 10.8
const strNum = '10.8'

Math.floor(num) // takes number and rounds it down

Math.round(num) // rounds down if below .5, rounds up if above or equal .5

Math.random() // creates a number between 0 and 1

Number(strNum) // converts a string number into an actual number

parseInt(stringNum) // goes up until first number that is not an int. so it would be 10 in this example

parseFloat(stringNum) // works the same but with float numbers

# BigInt

100n // you can declare a bigInt

BigInt(100) // 100n
