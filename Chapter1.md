**1.1. Writing a Simple C++ Program**
* `function`: return type, function name, parameter list, function body.

* Exercise Section 1.1.1
  * Exercise 1.1
    > .cpp
  * Exercise 1.2

**1.2. A First Look at Input/Output**
* header: `#include`
* `endl`: Flushing the buffer ensures that all the output the program has generated so far is actually written to the output stream, rather than sitting in memory waiting to be written.
* `namespace`: The prefix std:: indicates that the names cout and endl are defined inside the namespace named std. 
* Exercise Section 1.2
  * Exercise 1.3: Write a program to print Hello, World on the standard output.
    ```c++
    int main() {
      std::count << "Hello, World" << std::endl;
      return 0;
    } 
    ```
  * Exercise 1.4: Our program used the addition operator, +, to add two numbers. Write a program that uses the multiplication operator, *, to print the product instead.
    ```c++
    int main() {
      int one = 0;
      int two = 0;
      std::count << "Please input 2 nums" << std::endl;
      std::cin >> one >> two;
      std::count << one * two << std::endl;
      return 0;
    }
    ```
  * Exercise 1.5: We wrote the output in one large statement. Rewrite the program to use a separate statement to print each operand.
    ```c++
    std::cout << "The sum of " << v1 << " and " << v2 << " is " << v1 + v2 << std::endl;
    std::cout << "The sum of ";
    std::cout << v1;
    std::cout << " and ";
    std::cout << v2;
    std::cout << " is ";
    std::cout << v1 + v2 << std::endl;
    ```
  * Exercise 1.6: Explain whether the following program fragment is legal or not.
    ```c++
    std::cout << "The sum of " << v1; 
              << " and " << v2;
              << " is " << v1 + v2 << std::endl;
    ```
    > this is illegal.
**1.3 A Word about Comments**
* Exercises Section 1.3
  * Exercise 1.7: Compile a program that has incorrectly nested comments.
    ```c++
    int main()
    {
      cout<<"Hello World" << endl;
      /*
      * asd */
      *
      */

      return 0;
    }
    ```
    ```
    main.cpp:19:6: error: expected primary-expression before ‘/’ token
     19 |     */
        |      ^
    ```
  * Exercise 1.8: Indicate which, if any, of the following output statements are legal:
    ```c++
    Click here to view code image
    std::cout << "/*";
    std::cout << "*/";
    std::cout << /* "*/" */;
    std::cout << /* "*/" /* "/*" */;
    ```
    After you’ve predicted what will happen, test your answers by compiling a program with each of these statements. Correct any errors you encounter.
    ```c++
       17 |     std::cout << /* "*/" */;
          |                        ^
       main.cpp:17:24: error: missing terminating " character
    ```
