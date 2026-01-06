import'dart:io';
import'dart:math';
void main()
{
var  a ,x,y;
print("Enter what do you want to Do");
print(" 1.Add \n 2.Diference \n 3.Product \n 4.Division \n 5.Remender \n 6.square  \n 7.cude \n 8.sin value of x and  cos  value of y \n 9.cos value of x and sin value of y  ");
a =int.parse(stdin.readLineSync()!);
if(a<=9){
    print("enter the first number ");
    x =int.parse(stdin.readLineSync()!);
    print("enter the second number ");
        y =int.parse(stdin.readLineSync()!);

    switch(a){
     case 1:
     print("Sum is ${x+y}");
     break;
     case 2:
     if(x>y)
     print("Diffrence  is ${x-y}");
     else 
     print("Diffrence  is ${y-x}");
     break;
    case 3:
    print("Product is  ${x*y}");
    break;
    case 4:
    if(y==0)
    print("Denominator is 0 so it is not possible");
    else
    print("Division is ${x/y}");
    break;
    case 5:
    if(y==0)
    print("Denominator is 0 so it is not possible");
    else
    print("Remender is ${x%y}");
    break;
    case 6:
    print("Square of First  entered is ${pow(x,2)}  and of Second is ${pow(y,2)}");
    break;
    case 7:
    print("Square of First  entered is ${pow(x,3)}  and of Second is ${pow(y,3)}");
    break;
    case 8:
    print("sin($x)=${sin(x)} and Cos($y)=${cos(y)} ");
    break;

    case 9:
    print("cos($x)=${cos(x)} and sin($y)=${sin(y)} ");
    }
}
else
print("I am not  your calculator  Do  it your  self \n sala  dekh  k bhi jada bol raha hai");
}
