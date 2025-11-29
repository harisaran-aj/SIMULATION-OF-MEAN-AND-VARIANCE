# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB

## AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed

•	Computer with i3 Processor
•	SCI LAB


## Algorithm
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results


## PROGRAM

```
close;
clc;
close;

function X = f(x),
    z = 3 * (1 - x)^3,
    X = x * z
endfunction

a = 0;
b = 1;
EX = intg(a, b, f);

function Y = c(y),
    z = 3 * (1 - y)^3,
    Y = y * z
endfunction

EY = intg(a, b, c);

disp(EX, "i) Mean of X = ")
disp(EY, "Mean of Y = ")

function X = g(x),
    z = 3 * (1 - x)^3,
    X = x^2 * z
endfunction

a = 0;
b = 1;
EX2 = intg(a, b, g);

function Y = h(y),
    z = 3 * (1 - y)^3,
    Y = y^2 * z
endfunction

EY2 = intg(a, b, h);

vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;

disp(vX2, "ii) Variance of X = ");
disp(vY2, "Variance of Y = ");

x = input("type in the reference sequence = ");
y = input("type in the second sequence = ");

n1 = max(size(y)) - 1;
n2 = max(size(x)) - 1;

r = corr(x, y, n1);
plot2d3('gnn', r);

```
## CALCULATION
![WhatsApp Image 2025-11-29 at 10 10 55_a7828854](https://github.com/user-attachments/assets/4a73c9f2-d98d-457a-a787-c20fb03c4fa6)
![WhatsApp Image 2025-11-29 at 10 10 55_7b4b58fd](https://github.com/user-attachments/assets/3cf0f631-8e1b-4726-8261-d3c7bfbc7405)
![WhatsApp Image 2025-11-29 at 10 10 55_f95469c9](https://github.com/user-attachments/assets/c5205a38-3911-4295-8daa-90cebfa86667)


## OUTPUT

<img width="605" height="368" alt="image" src="https://github.com/user-attachments/assets/f1ecb60b-1e21-48e7-b15f-8320faccde67" />

<img width="758" height="718" alt="image" src="https://github.com/user-attachments/assets/705dfa6c-9f2e-4669-97e4-5d9078cff740" />

## RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
