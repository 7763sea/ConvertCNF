# ConvertCNF
**[Python3]** Convert DNF to satisfaction equivalent CNF with Tseitin algorithm implementation

## Input
Logical function written in the simplest DNF 
Example: **[[1,2],[-3]]**  
  It means **AB+C'** (' means NOT).  
  Each number represents a corresponding logical variable.  
  Minus signifies the negation of its logical variable.  

## Output
Satisfaction equivalent CNF converted with the following rules;  
**AB.. = (A'+B'+..+X)(A+X')(B+X')..**  
(X is new variable which does not affect the output of the function.
Introduce one new variable for each conversion.)  
Example: **[[-1,-2,4],[1,-4],[2,-4],[3,5],[-3,-5]]**   
  This result is the output to the above example of Input.  
  In this case, **(A'+B'+E)(A+E')(B+E')(C+F)(C'+F')** is the answer.

## Requirement
Nothing special

## Usage
First, place **Tseitin.py** in the same directory as the file in which 
you want to use this function (let's say **driver.py**).  
Or, you can make **Tseitin.py** be your own module.  
In **driver.py**,
- import Tseitin.py `import Tseitin`
- call Tseitin function `ans = Tseitin.Tseitin(dnf)`
- then, `ans` is the satisfaction equivalent CNF

## Confirmed Environment
OS: macOS Sierra 10.12.5  
Python: 3.6.3
