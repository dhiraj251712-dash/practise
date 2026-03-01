import 'dart:io';
import 'dart:math';

void main() {
  while (true) {
    print("\nEnter what do you want to do:");
    print("""
  1. Add
  2. Difference
  3. Product
  4. Division
  5. Remainder
  6. Square
  7. Cube
  8. sin(x) & cos(y)
  9. cos(x) & sin(y)
  0. Exit
""");

    stdout.write("Your choice: ");
    int a = int.parse(stdin.readLineSync()!);

    if (a == 0) {
      print("Exiting calculator. Bye dost! 👋");
      break;
    }

    if (a >= 1 && a <= 9) {
      stdout.write("Enter first number: ");
      int x = int.parse(stdin.readLineSync()!);

      stdout.write("Enter second number: ");
      int y = int.parse(stdin.readLineSync()!);

      switch (a) {
        case 1:
          print("Sum is ${x + y}");
          break;
        case 2:
          print("Difference is ${x > y ? x - y : y - x}");
          break;
        case 3:
          print("Product is ${x * y}");
          break;
        case 4:
          if (y == 0)
            print("Denominator is 0, division not possible");
          else
            print("Division is ${x / y}");
          break;
        case 5:
          if (y == 0)
            print("Denominator is 0, remainder not possible");
          else
            print("Remainder is ${x % y}");
          break;
        case 6:
          print("Square of first is ${pow(x, 2)}, of second is ${pow(y, 2)}");
          break;
        case 7:
          print("Cube of first is ${pow(x, 3)}, of second is ${pow(y, 3)}");
          break;
        case 8:
          double radX = x * pi / 180;
          double radY = y * pi / 180;
          print("sin($x°) = ${sin(radX)}, cos($y°) = ${cos(radY)}");
          break;
        case 9:
          double radX = x * pi / 180;
          double radY = y * pi / 180;
          print("cos($x°) = ${cos(radX)}, sin($y°) = ${sin(radY)}");
          break;
      }
    } else {
      print("Invalid choice 😅, I am not your calculator for this 😜");
    }
  }
}
