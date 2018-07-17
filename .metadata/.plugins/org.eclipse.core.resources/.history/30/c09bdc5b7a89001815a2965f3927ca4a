import java.util.Scanner;

public class Functions {

public static void main(String[] args) {
	
//text reader
Scanner reader = new Scanner(System.in);

while (reader.hasNextLine()) {

//function
String function = reader.nextLine();

//function = function.toUpperCase();

//if there is an error
boolean error = false;

//begin timer
final long startTime = System.currentTimeMillis();

//detects which function user wishes to perform
switch (function) {

case ("prime factors"): {
//prime factorization

//Stores the prime factor and its exponent
int factors[][] = new int[100][2];

//current numbered prime
int count = 0;

//current number/prime factor that is being check as a factor
int number;

//number being factored
long original = reader.nextLong();

//current number that is being divided
long product = original;


//prime factorizes the number and stores it in an array
if (original >= 2) {
while (product != 1) {

number = smallPFactor(product);

factors[count][0] = number;
factors[count][1]++;
product/=number;
if (product != 1) {

if (smallPFactor(product) != number) {

count++;
}
}
}

//prints out the prime factorization
System.out.print("The prime factorization of " + original + " is ");

for(int i = 0; i <= count; i++) { 
System.out.print(factors[i][0] + "^");
System.out.print(factors[i][1]);

if (i < count) {

System.out.print(" * ");

}
}

System.out.print(".\n");

} else {
//if the input was invalid

error = true;

System.out.println("Error.");

}



break;

} case ("prime list"): {

//lists all prime numbers up to a number


//lower and upper bound of prime list

long min = reader.nextLong();

long max = reader.nextLong();



boolean empty = true;



if (min <= max) {



if (min < 3) {

//much more optimized method



if (min < 0) {

min = 0;

}



if (max >= 2) {

System.out.println("2");

empty = false;

if (max > 2) {



double d = (max/2 + 1);

int l = (int)(Math.ceil(d));

long primes[] = new long[l];

primes[0] = 3;



int primeCount = 0;



for (int i = 3; i < max + 1; i+=2) {



int k = 0;

boolean isPrime = true;

while (primes[k] <= Math.pow(i, 0.5) && isPrime) {

if (i % primes[k] == 0) {

isPrime = false;

}

k++;



}

if (isPrime) {

primes[primeCount] = i;

System.out.println(i);

primeCount++;

}

}



}

}



} else {

if (min % 2 == 0) {

min++;

}



//checks for primes using the function primeCheck

//not so optimized method

for(long i = min; i < max + 1; i+=2) {

if(primeCheck(i)) {

System.out.println(i);;

empty = false;

}

}

}

if (empty) {

System.out.println("There are no prime numbers on the closed interval [" + min + "," + max + "].");

}

} else {

error = true;

System.out.println("Error.");

}



break;

} case ("prime check"): {

//checks if a number is prime



long number = reader.nextLong();



//check if the number is prime using the function primeCheck

if(primeCheck(number)) {

System.out.println(number + " is prime.");

} else {

System.out.println(number + " is not prime.");

}



break;

} case ("prime amount"): {

//returns amount of prime numbers on a closed interval



//instructions

System.out.println("Enter two non-negative integers a,b for the closed interval [a,b].");



//lower and upper bound of prime list

long min = reader.nextLong();

long max = reader.nextLong();



long amount = 0;



if (min <= max) {



if (min < 3) {

//much more optimized method



if (min < 0) {

min = 0;

}



if (max >= 2) {

amount++;

if (max > 2) {



double d = (max/2 + 1);

int l = (int)(Math.ceil(d));

long primes[] = new long[l];

primes[0] = 3;



int primeCount = 0;



for (int i = 3; i < max + 1; i+=2) {



int k = 0;

boolean isPrime = true;

while (primes[k] <= Math.pow(i, 0.5) && isPrime) {

if (i % primes[k] == 0) {

isPrime = false;

}

k++;



}

if (isPrime) {

primes[primeCount] = i;

primeCount++;

amount++;

}

}



}

}



} else {

if (min % 2 == 0) {

min++;

}



//checks for primes using the function primeCheck

//not so optimized method

for(long i = min; i < max + 1; i+=2) {

if(primeCheck(i)) {

amount++;

}

}

}

if (amount <= 0) {

System.out.println("There are no prime numbers on the closed interval [" + min + "," + max + "].");

} else if (amount == 1) {

System.out.println("There is one prime number on the closed interval [" + min + "," + max + "].");



} else {

System.out.println("There are " + amount + " prime numbers on the closed interval [" + min + "," + max + "].");

}

} else {

error = true;

System.out.println("Error.");

}



break;

} case ("prime number"): {

//returns the nth prime number

//the current and desired number place of the prime

int place = 1;

int n = reader.nextInt();



//the prime number

int number = 2;



while(place < n) {



number++;



if(primeCheck(number)) {

place++;

}

}



//different suffix depending on the ordinality of the place

if (n == 1) {

System.out.println("The 1st prime number is " + number + ".");

} else if (n == 2) {

System.out.println("The 2nd prime number is " + number + ".");

} else if (n == 3) {

System.out.println("The 3rd prime number is " + number + ".");

} else {

System.out.println("The " + n + "th prime number is " + number + ".");

}



break;

} case ("primorial"): {

//product of the first n primes; factorial but for prime numbers



//input

int n = reader.nextInt();



System.out.println(primorial(n));



break;

} case ("primorial check"): {

//a primorial prime is a prime that is in the form Pn# +- 1 where Pn# is the primorial of n



//input

long n = reader.nextInt();

//current primorialed number

int number = 0;

//type of primorial number (+/-/NA)

int type = 0;

if(primeCheck(n)) {

while(primorial(number) <= n + 1) {

if (n == primorial(number) + 1) {

System.out.println(n + " is a primorial prime (P" + number + "# + 1.");

} else if (n == primorial(number) - 1) {

System.out.println(n + " is a primorial prime (P" + number + "# - 1.");

}

number++;

}

} else {

System.out.println(n + " is not a primorial prime.");

}



break;

} case ("factorial"): {

//product of the first n natural numbers

int number = reader.nextInt();

System.out.println(number + "! is equal to " + factorial(number) + ".");



break;

} case ("combination"): {

//number of ways to take n objects from m total objects

int m = reader.nextInt();

int n = reader.nextInt();

System.out.println(m + " choose " + n + " is equal to " + factorial(m)/factorial(n)/factorial(m-n) + ".");



break;

} case ("permutation"): {

//number of ways to arrange n objects from m total objects

int m = reader.nextInt();

int n = reader.nextInt();

System.out.println(m + " pick " + n + " is equal to " + factorial(m)/factorial(m-n) + ".");



break;

} case (""): {

//empty case for enters

}



//if inputed text is not a function

default: System.out.println("Error. '" + function + "' is not a function.");

}



final long endTime = System.currentTimeMillis();

if (error == false) {

System.out.println("Total execution time: " + (endTime - startTime) + " miliseconds");

}

System.out.println("`````~");



}



reader.close();



}



static int smallPFactor (float number) {

int factor = 2;

while(number % factor != 0) {

factor++;

}

return factor;

}



static boolean primeCheck (long number) {

boolean isPrime = true;

float j = 2;



if (number < 2) {

return false;

} else if (number == 2) {

return true;

} else {

while(j <= Math.ceil(Math.pow(number, 0.5)) && isPrime) {

if(number%j == 0) {

isPrime = false;

}

j++;

}



return isPrime;

}

}



static long primorial (int n) {



//current place

int place = 0;

//the current prime number

int number = 1;

//the product

long product = 1;



while(place < n) {



number++;



if(primeCheck(number)) {

place++;

product*=number;

}

}

return product;

}



static long factorial (int number) {

//product of the first n natural numbers

//the current product

long product = 1;

if (number >= 2) {

for(int k = 2; k <= number; k++) {

product *= k;

}

}



return product;

}

}

