# -public class TriangleArea {
    public static double calculateArea(int x1, int y1, int x2, int y2, int x3, int y3) {
        return 0.5 * Math.abs((x1 * (y2 - y3) + x2 * (y3 - y1) + x3 * (y1 - y2)));
    }

    public static void main(String[] args) {
        int x1 = 1, y1 = 5;
        int x2 = 3, y2 = 5;
        int x3 = 6, y3 = 7;

        double triangleArea = calculateArea(x1, y1, x2, y2, x3, y3);
        System.out.println("Площадь треугольника: " + triangleArea);
    }
}
public class EvenOddCheck {
    public static void checkEvenOrOdd(int number) {
        if (number % 2 == 0) {
            System.out.println(number + " - четное число");
        } else {
            System.out.println(number + " - нечетное число");
        }
    }

    public static void main(String[] args) {
        int numberToCheck = 17;
        checkEvenOrOdd(numberToCheck);
    }
}
public class MinMagnitude {
    public static void printMinByMagnitude(double num1, double num2, double num3) {
        double[] numbers = {Math.abs(num1), Math.abs(num2), Math.abs(num3)};
        double minAbs = numbers[0];

        for (double num : numbers) {
            if (num < minAbs) {
                minAbs = num;
            }
        }

        if (minAbs == Math.abs(num1)) {
            System.out.println("Наименьшее число по модулю: " + num1);
        } else if (minAbs == Math.abs(num2)) {
            System.out.println("Наименьшее число по модулю: " + num2);
        } else {
            System.out.println("Наименьшее число по модулю: " + num3);
        }
    }

    public static void main(String[] args) {
        double num1 = -5, num2 = 7, num3 = 11;
        printMinByMagnitude(num1, num2, num3);
    }
}
import java.util.Scanner;

public class ReverseNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Введите число: ");
        int number = scanner.nextInt();

        int reversedNumber = 0;
        while (number != 0) {
            int digit = number % 10;
            reversedNumber = reversedNumber * 10 + digit;
            number /= 10;
        }

        System.out.println("Число в обратном порядке: " + reversedNumber);
        scanner.close();
    }
}
