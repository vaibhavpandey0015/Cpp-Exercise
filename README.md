# Cpp-Exercise
# Practice And Learn Cpp Code from basics to advance   


# Compare the different "Hello World!" Program
      
      #include<iostream>
      
      int main(int arge, const char* argv[])
      {
          std::cout << "Hello World!\n";
          return 0;
      }
 ---------------------------------------------------------------------------------------------------
     
      #include <iostream>
      
      int main()
      {
          std::cout << "Hello World!\n";
          return 0;
      }
 ---------------------------------------------------------------------------------------------------
     
      #include <iostream>
      using namespace std;
      
      int main()
      {
          cout << "Hello World!\n";
          return 0;
      }
 ---------------------------------------------------------------------------------------------------
     
      #include<cstdio>
      using namesapce std;

      int main() {
          puts("Hello World!\n");
          return 0;
      }
 ---------------------------------------------------------------------------------------------------
     
# Note
	1. Bjarne Stroustrue is a Danish Computer scientiest, most notable for the creation and development of the c++ programming language
	2. C++ is release in 1985.
	3. C++ is regarded as a middle-level language, as it comprises a combination of both high-level and low-level language features.
	4. <iostream>, <cstdio> is header files.
	5. using namespace std; tells the compiler to use the std namespace. If we do not write using namespace std; , then we have to write std:: before every standard fuctions from standard libraries.
		ex. std::cout<<"hello";
	6. main() is a single entry point in program.
	7. Semicolon is a statement terminator
	
# Note 2 (return keyword)

	After return keyword code does not run.
    return is at last.
    It resolves code collision.
    
# Note 3 (Primitive Built-in Data-Types) 

       Type                 |     Keyword
 	--------------------------------------------------------------------------              
     Boolean                |   bool
     Character              |   char
     Integer                |   int
     Floating point         |   float
     Double Floating Point  |   double
     Valueless              |   void
     -------------------------------------------------------------------------
       
    Basic types can be modified using one or more of these type modifiers:
    --->signed
    --->unsigned
    --->short
    --->long
---------------------------------------------------------------------------------------------------------------------
    
    char---|
    	   |--> unsigned char 	1 byte size and range is 0 to 255
    	   |--> signed char 	1 byte size and range is -127 to 127
    int -----|
             |--> unsigned int ------------------ 4 bytes size and range is 0 to 4,29,49,67,295
             |--> signed int -------------------- 4 bytes size and range is -2,14,74,83,648 to 2,14,74,83,647
             |
             |--> short int --------------------- 2 bytes size and range is -32,768 to 32,767
             |--> unsigned short in-------------- 2 bytes size and range is 0 to 65,535
             |--> signed short int -------------- 2 bytes size and range is -32,768 to 32,767
             |
             |--> long int ---------------------- 4 bytes size and range is -2,14,74,83,648 to 2,14,74,83,647
             |--> unsigned long int ------------- 8 bytes size and range is 0 to 4,29,49,67,295
             |--> signed long int --------------- 8 bytes size and range is -2,14,74,83,648 to 2,14,74,83,647
             |
             |--> long long int ----------------- 8 bytes size and range is -(2^63) to (2^63)-1
             |--> unsigned long long int -------- 8 bytes size and range is 0 to 18,44,67,44,073,70,95,51,615

    float --------> 4 bytes size	
    double -------> 8 bytes size	
    long double --> 12 bytes size
--------------------------------------------------------------

    #include<iostream>
    using namespace std;

    int main() {
        cout << "See the World..!\n";
        // It is single line Comment.
        /* This is multi line comments
            this is second line */

        bool isValid = true;
        char initial = 'v';
        int Number = 123;
        float decimalValue = 4.0008;
        double bigDecimalValue = 6.00000000000000000005;
        printf("Size of Boolean datatype is %ld bits. \n", sizeof(bool) * 8);
        printf("Size of Character datatype is %ld bits. \n", sizeof(char) * 8);
        printf("Size of Integer datatype is %ld bits. \n", sizeof(int) * 8);
        printf("Size of short Integer datatype is %ld bits. \n", sizeof(short int) * 8);
        printf("Size of long Integer datatype is %ld bits. \n", sizeof(long int) * 8);
        printf("Size of long long Integer datatype is %ld bits. \n", sizeof(long long int) * 8);
        printf("Size of long datatype is %ld bits. \n", sizeof(long) * 8);
        printf("Size of long long datatype is %ld bits. \n", sizeof(long long) * 8);
        printf("Size of Float datatype is %ld bits. \n", sizeof(float) * 8);
        printf("Size of Double datatype is %ld bits. \n", sizeof(double) * 8);

        return 0;
    }
    
# Pointer and Reference

	#include<iostream>
	#include<string>
	using namespace std;

	int main() {

		string person1 = "john";
		string person2 = "rita";

		string vip = person2;

		cout << "First Person is: " << person1 << endl;
		cout << "Seond Person is: " << person2 << endl;
		cout << "VIP person is: " << vip << endl;

		string* myptr;  //initilization the pointer
		myptr = &vip;   // store the address of vip in myp


		cout << "Address of VIP person is:" << myptr << endl;  // Print the address stored in myp
		cout << "VIP person is:" << *myptr << endl;  //Print the data of address stored in myp ==> It is also called Reference

		 
		cout << "...................................................." << endl;
		cout << "...................................................." << endl;

		string& another_address = vip;      // Now address of another_address and vip  is same 
		cout << "Address of VIP person is:" << &another_address << endl;
		cout << "VIP person is:" << another_address << endl;

		another_address = person1;  // if i change the value of another_adddress , vip will also change
									// any change in Reference changes a actual value
		cout << "Now VIP person is:" << vip << endl;
		cout << "Now VIP person is:" << another_address << endl;
		cout << "Now Address of VIP person is:" << &another_address << endl;

		cout << "VIP person is:" << *myptr << endl;

		return 0;
	}

# Array

	#include<iostream>
	using namespace std;

	int main() {

		/*Array Declaration*/

		int arr1[10];   //Declaration by specifying size
		int arr2[10] = { 11, 12, 13, 14, 15, 16, 17, 18, 19, 20}; //Declaration by specifying size and initializing elements
		int arr3[] = { 31,33,35,37 }; //Declaration by initializing elements

		/*Inserting element in array*/

		arr3[2] = 55;

		for (int i = 0; i < 10; i++) {
			arr1[i] = i + 1;
		}

		/*Access an array elements */
		cout << arr1[0] << " ";
		cout << arr1[1] << " ";
		cout << arr1[2] << " ";
		for (int i = 3; i < 10; i++) {
			cout << arr1[i] << " ";
		}

		return 0;
	}

# The elements are stored at contiguous memory locations in Array
	
	#include<iostream>
	using namespace std;

	int main() {

		cout << "Size of Interger data type is: " << sizeof(int) << " bytes" << endl;

		int interger_array[] = { 11, 12, 13, 14, 15, 16, 17, 18, 19, 20 };

		cout << "Address of First value (0th index) of an Array: " << interger_array << endl;   // It gives the address of initial value of an array
		cout << "First Value (0th index) of an Array: " <<*interger_array << endl << endl;  // Dereferance the address of initial value of an array

		int * home = interger_array;


		for (int i = 0; i < 10; i++) {
			cout << "Value at Address " << home + i << " is " << *(home + i) << endl << endl;
		}
		return 0;
	}
