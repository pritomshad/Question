[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/Kc_5KWsV)
<div align="center"><img src="sust-logo.png" width="100"></div>

Question Setter
---------------
Name:  **PRITOM DAS**         
Registration # **2021331039**            
Session: *2021-22*            
GitHub Username: *pritomshad*               
Cell: *01771856400*              
Email: *pritomd678@gmail.com*         

Question Set with Answers
=========================

<h2 align="center">Shahjalal University of Science and Technology
</h2>
<h3 align="center">Department of Computer Science and Engineering
</h3>
<div align="center"> 1<sup>st</sup> Year 1<sup>st</sup> Semester Final Examination &mdash;
June 2022 (Session 2021-22) </div>
<div align="center"> Course No. &mdash; <b> CSE 133</b> </div>
<div align="center"> Course Title &mdash; <b> Structured Programming Language</b> </div>
<div align="center"> Time &mdash; <b>  3 Hours</b> &nbsp;&nbsp;&nbsp;&nbsp; Credit: <b> 3.00</b>&nbsp;&nbsp;&nbsp;&nbsp;Total Marks # <b> 100</b></div>
<hr class="divider">
<div align="center"> (Answer All the Questions)</div><br>
<div align="center"><b>Group A</b> </div>
<div align="left">1. Answer the following Questions in short. (Any <b>Five</b>). &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5 &times; 2 = 10 </div>

(a) 
```c
int main() {return 0;}
```
is this a valid program? Note that we did not ` #include` any headers.</br>
    If this is not a valid program, what should we write to make it valid? </br>
    ***clarification:** valid means build successful and runs properly without errors</br>*
**Answer:**    <br>
We include headers for specific purposes. If we want to print something in the console</br>
we would include stdio.h. But it is upto the program maker to include something like this.</br>
If he does not intend to print something in the console he should not include stdio.h. This</br>
is a perfectly valid program.</br><br>
(b) Let `X` and `Y` be two intger values. `X=0x15` and `Y=0x1`. What should be the values of `X` and `Y` after</br>
    this statement is run? <br>
    ```
    Y^=X^=Y^=X^=Y^=X^=Y;
    ```<br>
**Answer:**<br>
this one is pretty straightforward. the last half `X^=Y^=X^=Y` swaps the values. After this operation the values<br>
are `X=0x1` and `Y=0x15`. then the values are again swapped by this `Y^=X^=Y^=X`. finally `X=0x15` and `Y=0x1`.<br><br>
    
(c) `~16 = 1111 1111 1110 1111` but it will return in `-17` when printing it. Can you suggest a way to print the original decimal value? i.e. the unsigned value. Here is the code example.
```c
printf("%d", ~16); //prints -17
```
**Answer:** <br>
just print it in unsigned mode.
```c
printf("%u", ~16);
```
(d)
```c
#define PI 3.14159
int main() {
    printf("%f",PI);
}
```
we all know the above program will print `3.141590`. if we use `%.4f` it will print `3.1416`.
You have to find a way to print this without rounding. i.e. the output should be
`3.1415`. *Note: you can not directly print `printf("3.1415")`. you have to use `PI`.* <br>
What would you change?<br>
**Answer:**<br>
chage the 3rd line to
```c
printf("%.4f", ((float)(int)(PI * 10000)) / 10000);
```
<br><br>
(e) What is the highest number we can store using a `nibble` of memory space? If we do not consider the sign(+ or -) of our number then<br>
what will be the highest number we can store using a `nibble` of memory space?<br>
**Answer:**<br>
A nibble is 4-bits.if we consider sign(+-) we need a bit at the beginning to indicate it. So we are left with 3 bits.<br> 
highest number a 3-bit can store is `111` in binary and `7` in decimal. But without the sign digit we can use 4-bits thus
can store upto `1111` which is `15`.<br>
(f) there is a comma-separated line you have to take input from. Example: `pritom das, 001teribehennko_ naman!@#$% (*), 134642`. As you can see this has 2 commas separating the string into 3 parts. Write a `scanf()` function to take the input and store the first part in `name`, the middle part in `bla` and the third part in an integer variable `k`.<br>
**Answer:** <br>
```c
    scanf("%[^,]%*c%[^,]%*c%d", name, bla, &k);
```
*Clarification: `%*c` is to ignore the commas(,).* <br>
(g) Read the code snippet carefully.
```c
long long k, *p, **pp, ***ppp;
k=92193; *p=&k; **pp=&p; ***ppp=&pp;
printf("%d",sizeof(***ppp));
```
what will be the output?<br>
**Answer:** <br>
`***ppp` is addressing finally to `k`. `k` is `long long` thus output is: `8`<br>
(h) `morty[34][33][32]` is a three-dimensional array. Access the very last element of this array using pointers. <br>
**Answer:** <br>
`*(*(*(morty+33)+32)+31)` : This will access the last element;

<div align="left">2. Answer the following Questions. (Any <b>Four</b>). &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4 &times; 5 = 20 </div>

(a)
```c
typedef struct {
    char name[10];
    int age;
} person;
person list[23][2][3][4];
```
if `list[0][0][0][0]` memory address is `0x1`; What should be the memory address of `list[21][0][1][0]`?<br>
**Answer:**<br>
let's figure out the offset. <br>
`offset = 21*2*3*4 + 0*3*4 + 1*4 + 0 = 508`<br>
now multiply offset by `sizeof(person)` which is `508*14 = 7112`.<br>
let's add it to the initial value `0x1`<br>
the answer will be `hex(1+7112) = 0x1bc9`<br><br>
(b) 
```c
#include <stdio.h>

int main() {
    char *p = "Rick and Morty season 3";
    char **pp = &p;
    printf("%s",**pp);
    return 0;
}
```
<br> is this a valid program? If it is, what will be the output? If not, correct this program to get the desired output.<br>
**Answer:** <br>
this is not a valid program and will cause a `Segmentation error`. Let's consider a simple example. if we declare a `char *s = "pritom das"`, how we will print this statement?
`printf("%s", s):`. As we can see when printing a string we are writing the pointer directly in the printf function. The correct ans for the following program will be: `printf("%s",*pp);` this will print `Rick and Morty season 3`.<br>
(c) you are given a `m x n` matrix with integer values in it. Write a program to make it a corner matrix. It means just the corner values should be stored unchanged other values should be set to 0.
<br> **Answer:** <br>
```c
int matrix[m][n];
for (int i=0; i<m; i++)
    for (int j=0; j<n; j++)
        if (i!=j) matrix[i][j]=0;
```
(d) Write a program to calculate the area under graph f(x)=e<sup>x</sup>. The user will input the range `a b`. you should print the value of area from `a` to `b` under the graph f(x)=e<sup>x</sup>.
<br>**Answer:** <br>
```c
#include<stdio.h>
#include<math.h>
int main() {
    double a, b;
    scanf("%lf %lf", &a, &b);
    printf("%lf", exp(b)-exp(a));
}
```
(e) We all know that e<sup>-x<sup>2</sup></sup> is not integrable. But it has area value. The graph is shown below for a better understanding. Your work is to find the area under the curve given a range `x= (a to b)` where `a<b` and `|a|, |b|<3`. To make this easier, your output precision value should not be greater than 2 digits after the decimal point.<br>
![image](https://github.com/cse-133-2021/question-setting-with-answer-pritomshad/assets/59039346/eeea0209-073a-4ae0-99df-a5dc8c8b51e3)
<br> **Answer:** <br>
```c
#include<stdio.h>
#include<string.h>
#include<math.h>
double f(double x) {
	return exp(-x*x); //e^(-x^2)
}
int main() {
	double a,b;
	scanf("%lf %lf", &a, &b);
	a*=1000.;
	b*=1000.;
	double area=0, temp_a=a, temp_b=b;
	while(1) {
		a+=1.;
		area+=((f(a/1000.)+f(temp_a/1000.))/2.)*(a/1000.-temp_a/1000.);
		temp_a = a;
		if(a==b) break;
	}
	printf("%lf\n", area);
	return 0;
}
```
(f) take integer input without using scanf(). By passing arguments through main(). there would be at most 100 integers. Print then using `printf("%d\n",number);`.
```c
#include<stdio.h>
#include<string.h>
#include<math.h>
#include<stdlib.h>

int main(int arg_c, char *arg_v[]) {
	int a[101];
	for (int i=0; i<arg_c; i++) {
		a[i] = atoi(arg_v[i]);
	}
	for (int i=0; i<arg_c; i++) {
		printf("%d\n", a[i]);
	}
	return 0;
}
```
<div align="left">3. Answer the following Questions. (Any <b>Two</b>). &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2 &times; 10 = 20 </div>

(a) Print a circle. (too easy). get `r` input from user. The radius of the circle should be `r`. here is a example output for `r=5`.
```
        *     *       
       *       *      
                      
                      
      *         *     //notice that in this line there are 10 spaces between asterisks. 2*r = 2*5 =10
                      
                      
       *       *      
        *     *       
           *          
```
<i>hint: use the basic theory for circles x<sup>2</sup>+y<sup>2</sup>=r<sup>2</sup> </i>
**Answer** <br>
```c
#include<stdio.h>
int main() {
    double r;
    scanf("%lf",&r);
    for (int i=-2*r-1; i<2*r+1; i++) {
        for (int j=-2*r-1; j<2*r+1; j++) {
            if (i*i + j*j == r*r) printf("*");//here we used the basic circle theory
            else printf(" ");
        }
        printf("\n");
    }
}
```
(b) The following line is an encrypted text.
```
5 59 26 58 24 6 23 55 10 59 4 1 2 1 4
```
You have to decode it. As a computer science student, you should automate your decoding by writing a program. The encoding is done by this code:
```c
#include<stdio.h>
#include<string.h>
enum alphabet {
    a=1,b,c,d,e,f,g,h,i=54,j,k,l,m,n,o,p,q=22,r,s,t,u,v,w,x=10,y,z
};
int main() {
    char *text = "here goes the text you want to encrypt";
    for(int i=0; i<strlen(text);i++)
        switch(text[i]) {
            case 'a':printf("%d ",a);break;
            case 'b':printf("%d ",b);break;
            case 'c':printf("%d ",c);break;
            case 'd':printf("%d ",d);break;
            case 'e':printf("%d ",e);break;
            case 'f':printf("%d ",f);break;
            case 'g':printf("%d ",g);break;
            case 'h':printf("%d ",h);break;
            case 'i':printf("%d ",i);break;
            case 'j':printf("%d ",j);break;
            case 'k':printf("%d ",k);break;
            case 'l':printf("%d ",l);break;
            case 'm':printf("%d ",m);break;
            case 'n':printf("%d ",n);break;
            case 'o':printf("%d ",o);break;
            case 'p':printf("%d ",p);break;
            case 'q':printf("%d ",q);break;
            case 'r':printf("%d ",r);break;
            case 's':printf("%d ",s);break;
            case 't':printf("%d ",t);break;
            case 'u':printf("%d ",u);break;
            case 'v':printf("%d ",v);break;
            case 'w':printf("%d ",w);break;
            case 'x':printf("%d ",x);break;
            case 'y':printf("%d ",y);break;
            case 'z':printf("%d ",z);break;
        }
}
```
<br> **Answer:** <br>
this decoded text is `enum sir jindabad` <br>
```c
#include<stdio.h>
#include<string.h>
enum alphabet {
    a=1,b,c,d,e,f,g,h,i=54,j,k,l,m,n,o,p,q=22,r,s,t,u,v,w,x=10,y,z
};
int main() {
    for(int kkk=0; kkk<15; kkk++) {
        int temp;
        scanf("%d",&temp);
        char letter;
        switch(temp) {
            case a: letter = 'a'; break;
            case b: letter = 'b'; break;
            case c: letter = 'c'; break;
            case d: letter = 'd'; break;
            case e: letter = 'e'; break;
            case f: letter = 'f'; break;
            case g: letter = 'g'; break;
            case h: letter = 'h'; break;
            case i: letter = 'i'; break;
            case j: letter = 'j'; break;
            case k: letter = 'k'; break;
            case l: letter = 'l'; break;
            case m: letter = 'm'; break;
            case n: letter = 'n'; break;
            case o: letter = 'o'; break;
            case p: letter = 'p'; break;
            case q: letter = 'q'; break;
            case r: letter = 'r'; break;
            case s: letter = 's'; break;
            case t: letter = 't'; break;
            case u: letter = 'u'; break;
            case v: letter = 'v'; break;
            case w: letter = 'w'; break;
            case x: letter = 'x'; break;
            case y: letter = 'y'; break;
            case z: letter = 'z'; break;
        }
        printf("%c", letter);
    }
}
```
(c) There is a car-selling company. They want to automate their business. Which is like this: The customers should be identified using their Telephone numbers. And for each customer, they told the programmer to create a (`.in`) file to store the customer's name and address. The name of the file should be the Telephone number. But The previous programmer working in the company made a mistake. Instead of using a Telephone number as the unique identification number he used the`customer name`. Now the same named persons are conflicted. Suppose There are 3 people named `Rick`. As the previous code it resulted in a `Rick.in` file. In that file, the telephone numbers and addresses are stored like this:
```
88017712, Housing estate
88017760, Mortgage
88053421, Siver town
```
you are hired to find a remedy for this. DO YOUR MAGIC!!! <i> Clarification: all the `.in` files and your `.c` program are stored in the same directory</i>
<br> **Answer:** <br>
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_FILENAME_LENGTH 1000
#define MAX_LINE_LENGTH 1000

void create_fixed_files() {
    // Open the current directory
    DIR* dir = opendir(".");

    // Create the FixedFiles directory if it doesn't exist
    mkdir("FixedFiles", 0700);

    // Iterate over the directory entries
    struct dirent* entry;
    while ((entry = readdir(dir)) != NULL) {
        char* filename = entry->d_name;
        size_t filename_len = strlen(filename);

        // Check if the entry is a ".in" file
        if (filename_len > 3 && strcmp(&filename[filename_len - 3], ".in") == 0) {
            // Extract the customer name from the file name
            char* customer_name = strtok(filename, ".");

            // Open the original file
            FILE* original_file = fopen(filename, "r");
            if (original_file == NULL) {
                printf("Failed to open file: %s\n", filename);
                continue;
            }

            // Read the telephone number and address from the original file
            char line[MAX_LINE_LENGTH];
            char TEL[100][100], ADDR[100][100];
            int c=0;
            while(fgets(line, sizeof(line), original_file)!=NULL){
                TEL[c] = strtok(line, ",");
                ADDR[c++] = strtok(NULL, ",");
            }

            // Create a new file with a unique name based on the telephone number
            for (int itr=0; itr<c; i++) {
                char new_filename[MAX_FILENAME_LENGTH];
                snprintf(new_filename, sizeof(new_filename), "FixedFiles/%s.in", TEL[itr]);
    
                // Open the new file
                FILE* new_file = fopen(new_filename, "w");
                if (new_file == NULL) {
                    printf("Failed to create file: %s\n", new_filename);
                    fclose(original_file);
                    continue;
                }
    
                // Write the customer name and address to the new file
                fprintf(new_file, "%s, %s", customer_name, address);
                fclose(new_file);
            }

            // Close the files
            fclose(original_file);
            printf("Fixed file created: %s\n", new_filename);
        }
    }

    // Close the directory
    closedir(dir);
}

int main() {
    create_fixed_files();
    return 0;
}

```
<div align="center"><b>Group B</b> </div>
<div align="left">1. Answer the following Questions in short. (Any <b>Five</b>). &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5 &times; 2 = 10 </div>

(a) The following is a structure `bee`.
```c
struct bee{
	int honey;
 	struct bee *next;
};
struct bee queen, *p, **pp, ***ppp;
*p = &queen;
pp = &p;
ppp = &pp;
```
you have some options to access the `queen.honey`. (1) `ppp->honey` (2) `(**ppp)->honey` (3) `pp->honey` (4) `p->honey` (5) `(*pp)->honey` (6) `(**pp).honey`
which options are correct for accessing the desired `honey`?
<br> **Answer:** <br>
```
(1) incorrect;
(2) correct;
(3) incorrect;
(4) correct;
(5) correct;
(6) correct;
```

(b) look carefully at the following code:
```c
#define multiply(a,b) (a*b)%100
int x = multiply(10+3, 10-7);
```
what is the value of x? Does this code serve the purpose of `(a*b)%100`?
<br> **Answer:** <br>
the value of x is 10+3*10-7 = 10+30-7 = 33. But this code does not serve the purpose of `(a*b%100)`. the correct definition would be:
```c
#define multiply(a,b) ((a)*(b))%100
```
(c) what should be the return value of `1<<4<<1<<4>>1`? Can you show the equivalent of this statement using brackets?
<br> **Answer:** <br>
let's show this statement using brackets. `(((1<<4)<<1)<<4)>>1` <br>
now 1<<4 is 16. 16<<1 is:<br>
16 = 10000<br>
16<<1 = 100000 = 32 <br>
32<<4 = 1000000000 = 512 <br>
512>>1 = 100000000 = 256 <br>
the answer is 256.<br>
(d) "Arrays are glorified Pointers". Write a simple program to take `100` integer values as input and print them afterward. But you cannot use Arrays. Write it only using pointers.
```c
#include <stdio.h>
#include<stdlib.h>
int main() {
    int *p = (int *) malloc(100*sizeof(int));
    for (int i=0; i<10; i++) {
        scanf("%d", p+i);
    }
    for (int i=0; i<10; i++) {
        printf("%d ", *p+i);
    }
    return 0;
}
```
(e) `0x1545` is a hex value. What should be the output of this: `0x1545<<2 & 0x3 ^ ~1<<4` <br> **Answer:** <br>
```
0x1545            0001 0101 0100 0101   ----(i)
(i)<<2            0101 0101 0001 0100   ----(ii)
0x3 = 	    	  0000 0000 0000 0011   ----(iii)
(ii) & (iii)      0000 0000 0000 0000	----(iv)
~1                1111 1111 1111 1110   ----(v)
~1<<4             1111 1111 1110 0000   ----(vi)
(iv)^(vi)         0000 0000 0001 1111
______________________________________
answer = 			   31
```
(f) Can you identify the mistake made in this code:
```c
#include<string.h>
int main(int arg_c, char *arg_v[]) {
	int len = strlen(arg_v[1]);
	return len;
}
```
If there is no mistake made in this piece of code what should be the output in the terminal/command prompt after each line is written and pressed enter? After building this program we run it in the terminal/command line like this:
```cmd
$ gcc filename.c -o a
$ ./a heygoogle
$ echo $?
```
<br> **Answer:** <br>
there is no mistake in this code. `#include<stdio.h>` is not a necessity for a successful code running. `main(int arg_c, char *arg_v[])` here we can see arguments passing through the main function. `int len = strlen(arg_v[1]);` this line is taking the 1st argument and getting its string length putting it in `len` variable. we are returning the `len`. When we build there would be no errors.`./a heygoogle` here we can see the 1st argument through the main function is `heygoogle`.
length of `heygoogle` is 9. thus `echo $?` will return 9 in the cmd/console/terminal.
(g) what is the Binary value of this octal value: `7231733463731516354`? <br> **Answer:** <br>
```
111 010 011 001 111 011 011 100 110 011 001 101 001 110 011 101 100
```
(h) Write a program to convert hexadecimal to decimal. <br> **Answer:** <br>
```c
int a;
scanf("%x",&a);
printf("%d",a);
```


<div align="left">2. Answer the following Questions. (Any <b>Four</b>). &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4 &times; 5 = 20 </div>

(a) 
```c
#include<stdio.h>
int main() {
    short int i,j,k,l,m,n,o,p;
    i=0; j=1; k=0; l=1; m=0; n=1; o=0; p=1;
    if(i || j) {
        printf("HEY rick!\n");
        if(k && l) printf("HEY Summer!\n");
        else{
            if(m||n) printf("Taylor Swift\n");
            if(o&&p) printf("Tagore\n");
        }
    }
    if(i&&j) printf("HEY pritom!\n");
    else {i=1;}
    if(i&&j) printf("HEY Morty!\n");
    else {i=0;}
    if(i&&j) printf("HEY Morty!\n");
    else {i=1;}
}
```
what will be the output of this program?
<br> **Answer** <br>
```
HEY rick!
Taylor Swift
HEY Morty!
HEY Morty!
```
(b) Rewrite the following program using only a single `#define`.
```c
int axolotl(char *lion, int mint) {
    int t=0;
    for(int it=0; it<mint; it++){
        if(lion[it]='a') t++;
    }
    return t;
}
```
**Answer:**

```c
#include<stdio.h>
#include<string.h>
#define AXOLOTL(lion, mint) ({          \
    int t = 0;                          \
    for (int it = 0; it < mint; it++) { \
        if (lion[it] == 'a') t++;       \
    }                                   \
    t;                                  \
})
int main() {
    char *boson = "amiamaraaami";
    int d = AXOLOTL(boson, strlen(boson));
    printf("%d\n",d);

    return 0;
}
```
(c) Write the output for the following program:
```c
#include <stdio.h>
int main() {
    int num[10]={1,2,3,4,5,6,7,8,9,10};
    int *p[10];
    int **pp[10];
    for (int i=0; i<10; i++) {
        int *temp = num+i;
        p[i] = num+i;
        pp[i] = &temp;
        printf("%d ",**pp[i]);
    }
    puts("");
    for (int i=0; i<10; i++) {
        printf("%d ",**pp[i]);
        pp[i] = &p[i];
    }
    puts("");
    for (int i=0; i<10; i++) {
        printf("%d ",**pp[i]+1);
    }
    
    return 0;
}
```
**Answer:** <br>
```
1 2 3 4 5 6 7 8 9 10 
10 10 10 10 10 10 10 10 10 10 
2 3 4 5 6 7 8 9 10 11
```
(d) 
Suppose you live in a world where Gravity is not constant. It has a random value each second. But it never drops below 9ms<sup>-2</sup> and never exceeds 10 ms<sup>-2</sup>. You are ordered to climb a stair for `n` seconds. Each staircase has height of `15 cm`. As Gravity is not constant the work done by you is also not constant each second. Your weight is 66kg. Write a program that will output your average Work done whilst climbing the stair.<i>Hint: use rand()</i>
<br>
**Answer:** <br>
```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

double fun(int n) {
    double total_work=0.0;

    for (int i = 0; i < n; i++) {
        double gravity = (rand() % 101 + 900) / 100.0;  // Random gravitational acceleration between 9 and 10
        double work = 66 * gravity * 0.15;  // Work done = force * distance, where distance = 0.15m

        total_work+=work;
    }

    double average_work=total_work/n;
    return average_work;
}

int main() {
    int n;
    scanf("%d", &n);

    // Seed the random number generator
    srand(time(0));

    double average_work = fun(n);
    printf("%.4lf\n", n, average_work);

    return 0;
}
```
(e) print this following pattern.<br>
n = 3
```
     *---*
  *---* *---*
*---*     *---*
  *---* *---*
     *---*
```
n=4
```
       *---*
    *---* *---*
  *---*     *---*
*---*         *---*
  *---*     *---*
    *---* *---*
       *---*
```
```
         *---*
      *---* *---*
    *---*     *---*
  *---*         *---*
*---*             *---*
  *---*         *---*
    *---*     *---*
      *---* *---*
         *---*
```
**Answer:**
```c
#include<stdio.h>
void pat(){printf("*---*");}
int main(int arg_c, char *arg_v[]) {
	int n;
	scanf("%d",&n);
	for (int i=0; i<n; i++) {
		if(i==0) {
			for (int j=0; j<2*n-1;j++) printf(" ");
			pat();
		}
		else {
			for (int j=0; j<2*(n-i-1);j++) printf(" ");
			pat();
			for (int j=0; j<(4*i)-3;j++) printf(" ");
			pat();
		}
		puts("");
	}
	for (int i=n-2; i>=0; i--) {
		if(i==0 || i==2*n-2) {
			for (int j=0; j<2*n-1;j++) printf(" ");
			pat();
		}
		else {
			for (int j=0; j<2*(n-i-1);j++) printf(" ");
			pat();
			for (int j=0; j<(4*i)-3;j++) printf(" ");
			pat();
		}
		puts("");
	}
	return 0;
}
```
(f) There is a popular game named Minecraft. You can open a server for the game, where multiple people can play together. The server costs money. Suppose you own a server and rented it to at most 1000 players. You get a log message file `server_log.in` every month. In that log there is player information who joined your server. You have to charge them .1$/hour. The server log looks like this:
```
prit0m 12/2/2023 2h
JAC_Sadi 13/4/2023 3h
JAC_Sadi 19/4/2023 3h
MAlihapa 11/9/2023 4h
prit0m 13/2/2023 1h
```
every user has a unique username. you have to store all users' monthly bills in a separate file called `bill.csv`. Like this:
```
prit0m, 0.2$
JAC_Sadi, .6$
MAlihapa, .4$
```
**Answer:** <br>
```c
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
typedef struct customer {
	char username[100];
	double total_useage;
} people;
int main() {
	people arr[1000];
	int itr=0;
	FILE *in, *bill;
	in = fopen("server_log.in","r+");
	bill = fopen("bill.csv","w+");
	for(int i=0; i<1000; i++) arr[i].total_useage=0;

	char line[1000];
	while(fgets(line, 1000, in)!=NULL) {
		char *temporary = strtok(line, " ");
		//printf("%s\n", temporary);
		char *name = temporary;
		temporary = strtok(NULL, " ");
		temporary = strtok(NULL, " ");
		temporary[strlen(temporary)-2]='\0';

		int chk = 1;

		for (int i=0; i<itr; i++) {
			if(strcmp(arr[i].username,name)==0) {
				arr[i].total_useage += atoi(temporary)*0.1;
				chk=0;
			}
		}
		if(chk) {
			strcpy(arr[itr].username, name);
			arr[itr++].total_useage = atoi(temporary)*0.1;
		}		
		
	}
	for (int i=0; i<itr; i++) {
			fprintf(bill,"%s, %lf$\n", arr[i].username, arr[i].total_useage );
	}
	fclose(in);
	fclose(bill);
	return 0;
}
```
<div align="left">3. Answer the following Questions. (Any <b>Two</b>). &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2 &times; 10 = 20 </div>

(a)   
```c
#include<stdio.h>
int main() {
    short int i,j,k,l,m,n,o,p;
    scanf(%d%d%d%d%d%d,&i, &j, &k, &l, &m, &n, &o, &p);
    if(i || j) {
        printf("HEY rick!\n");
        if(k && l) printf("HEY Summer!\n");
        else{
            if(m||n) printf("Taylor Swift\n");
            if(o&&p) printf("Tagore\n");
        }
    }
    if(i&&j) printf("HEY pritom!\n");
    else {i=1;}
    if(i&&j) printf("HEY Morty!\n");
    else {i=0;}
    if(i&&j) printf("HEY Morty!\n");
    else {i=1;}
}
```
Re-write this program using the `switch` statement such that the underlying logic is unchanged.
<br> **Answer:** <br>
```c
#include<stdio.h>
int main() {
    short int i,j,k,l,m,n,o,p;
    scanf(%d%d%d%d%d%d,&i, &j, &k, &l, &m, &n, &o, &p);
    switch(i || j) {
        case 1:
            printf("HEY rick!\n");
        switch(k && l) {
            case 1: 
                printf("HEY Summer!\n");
                break;
            default:
                switch(m||n) {
                    case 1:
                        printf("Taylor Swift\n");
                }
                switch(o&&p) {
                    case 1:
                        printf("Tagore\n");
                }
        }
    }
    switch (i && j) {
        case 1:
            printf("HEY pritom!\n");
            break;
        default:
            i = 1;
    }

    switch (i && j) {
        case 1:
            printf("HEY Morty!\n");
            break;
        default:
            i = 0;
    }

    switch (i && j) {
        case 1:
            printf("HEY Morty!\n");
            break;
        default:
            i = 1;
    }
}
```
(b) `rick[a][b][c]` is an array of characters. Here are some arbitrary memory addresses of the array `&rick[0][0][0]= 23`, `&rick[22][0][0]= 4423`, `&rick[1][2][0]= 227`, `&rick[0][102][c]= 229`, `&rick[a][b][c]= 10225`. Find the values of `a`,`b` and `c`. 
<br> **Answer:** <br>
we can extract equations:
```
22*b*c + 23 = 4423
1*b*c + 2*c + 23 = 227
102*c + c + 23 = 229
a*b*c + b*c + c + 23 = 10225
```
thus c = 2 <i>from equation 3</i>
now,
```
22*b*2 + 23 = 4423
=> b = 100
```
from the last equation:
```
a*200+200+2+23=10225
=> a= 50
```
thus `(a,b,c)=(50,100,2)`<br>
(c)  Make a C program that you can run anywhere on your pc -- to find out if any `.html` file contains any malicious links. Links in `html` are usually written like this
```html
<a target="_blank" href="http://www.facebook.com/">Click here for Facebook</a>
```
a malicious link is such link which does not go to the desired website and ends with `.onion` instead of `.com or .gov`. Now if anyone tries to hack you they will want to redirect you to their `.onion` website. The `html` for that is straight forward.
```html
<a target="_blank" href="http://1343fKfhiweKJSHwqkJewiH4249503Hiiiiii.onion/">Click here for Facebook</a>
```
you will click <a target="_blanck" href="https://pritomshad.github.io/mywebsite">Click here for Facebook<a> but it will redirect you to their website.<br>
If the `index.html` contains any malicious links warn the user using your program. Your program should take the `.html` file name as a console input. example:
```
$ ./malicious_link_check random_html_file.html
```
here `malicous_link_check` is your program name.(which is the binary layed by your c program)
<br> **Answer** <br>
```c
#include<stdio.h>
#include<string.h>

int main(int arg_c, char *arg_v[]) {

	FILE *web=NULL;
	web = fopen(arg_v[1], "r+");
	if(web==NULL) {
		puts("can't open file.");
		return 0;
	}
	
	char line[1000];
	char *mal = ".onion";
	char *check = NULL;
	while (fgets(line, 1000, web)!=NULL) {
		
		check = strstr(line, mal);
		if(check!=NULL) {
			puts("HEY Malicious site found! Don't go there.");
			break;
		}
		
	}
	if(check==NULL) printf("This file is okay to open.\n");

	return 0;
}
```

<div align="center">- End -</div>

- [x] I am declaring that, the above work is my own work. Whatever added above
except the template is the result of my brainstorming. I also understand that
submitting work that isn’t my own may result in permanent failure of this course
as well as the whole current semester.
