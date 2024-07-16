# Assembly Projects
Below you can find links to my various x86 Assembly projects, or just read their READMEs here.

## Project Links

### [Sum and Average Calculator](https://github.com/flwrr/Sum-and-Average-Calculator)
Calculate sums and averages of integer and floating-point numbers using both the CPU and [FPU](https://en.wikipedia.org/wiki/Floating-point_unit).

### [Prime Generator](https://github.com/flwrr/Prime-Generator)
Calculate up to 4000 primes using the [Sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes), and visualize the sieve generated.

### [RNG Sorter](https://github.com/flwrr/RNG-Sorter)
Generates random numbers between a set range, then uses merge sort to arrange them in non-descending order.<br>
<br>

## Project READMEs
- [Sum and Average Calculator](#sum-and-average-calculator-1)
- [Prime Generator](#prime-generator-1)
- [RNG Sorter](#rng-sorter-1)
- [Running the Projects](#running-the-projects)

<br>

# Sum and Average Calculator
As an exercise to explore the differences between integer and floating-point arithmetic in assembly, this program calculates the sums and averages of 10 imput integers using the CPU and 10 input floating-point numbers using the [FPU](https://en.wikipedia.org/wiki/Floating-point_unit). For both, the program first converts user input from strings to numbers while validating input, then calculates their sum and average, finally displaying formatted results for 10 input values.



## :large_orange_diamond: Run Example - Integers
This portion of the program is fairly straightforward and is capable of processing the full range of 32-bit signed integers from -2,147,483,648 to 2,147,483,647. The most challenging aspect was parsing + and - signs from input, and the logic of deciding when to and when not to display them to the user (e.g., not -0 nor +0).

![Calc_Integers-crop](https://github.com/user-attachments/assets/0f27d696-5ed5-4d83-8f13-b2df10b30e05)


## :fish: Run Example - Floating Point Numbers
Using the FPU, this portion of the program accepts signed inputs with up to 5 decimal places. A very memorable lesson on floating-point arithmetic and floating-point errors. Working with the FPU and fixing rounding errors without looking much up was a challenging exercise.

![Calc_FloatingPoint](https://github.com/user-attachments/assets/0888abb5-ab1b-4897-adca-8d8afcbe87e8)

<br>

# Prime Generator
This assembly language program calculates up to the first 4000 prime numbers using the [Sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes).The sieve formed in generating the n number of primes can be viewed afterward by pressing 'x', each array index stores either a 1 marking a prime or a 0 marking a non-prime, beginning with 0.

![Alt Text](https://upload.wikimedia.org/wikipedia/commons/b/b9/Sieve_of_Eratosthenes_animation.gif)
## :large_orange_diamond: Run Example

![primeGenerator](https://github.com/user-attachments/assets/90deabd3-11da-4c38-952f-174cc011ca63)

<br>

# RNG Sorter
This program generates random numbers between a set range, then uses merge sort to arrange them in non-descending order. After displaying the sorted array, the program then displays how many times each integer within the provided range appeared.

The number of values is preset to 200 and their range preset to between 15 and 50, but these can be adjusted by changing the global variables `ARRAYSIZE`, `LO`, and `HI`.

## :large_orange_diamond: Run Example
![RNG_Sorter-cropped](https://github.com/user-attachments/assets/7514edac-5b3b-46de-af69-e0d00d61402d)



<br>

# Running the Projects
  - Running any of these projects requires [Visual Studio ](https://visualstudio.microsoft.com/) with "Desktop development with C++", which includes MASM
  - Open the .sln file located in the root of the cloned repository
  - Right-click on the solution in the Solution Explorer and select Build Solution or press Ctrl+Shift+B
  - Set the project as the startup project by right-clicking on it in the Solution Explorer and selecting Set as Startup Project
  - Press F5 or click the `Start Debugging` button to run the program
