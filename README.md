# Java-tasks-2024-OOP
Habr 10 ENU 2024

### 1) Задача: Заполните массив случайным числами и выведите максимальное, минимальное и среднее значение. Для генерации случайного числа используйте метод Math.random(), который возвращает значение в промежутке [0, 1].




public class lib{
    public static void main(String[] args) {

        int n = 100;
        double[] array = new double[n];
        for (int i = 0; i < array.length; i++) {
            array[i] = Math.random();
        }

        double max = array[0];
        double min = array[0];
        double avg = 0;
        for (int i = 0; i < array.length; i++) {
            if(max < array[i])
                max = array[i];
            if(min > array[i])
                min = array[i];
            avg += array[i]/array.length;
        }

        System.out.println("max = " + max);
        System.out.println("min = " + min);
        System.out.println("avg = " + avg);
    } }
    
### Задача: Реализуйте алгоритм сортировки пузырьком для сортировки массива

public class lib {
    public static void main(String[] args) {
        double[] array = {5, 3, 7, 1, 2}; 
        
        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array.length - i - 1; j++) {
                if (array[j] > array[j + 1]) {
                    double temp = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = temp;
                }
            }
        }
        
        System.out.println("Sorted array:");
        for (int i = 0; i < array.length; i++) {
            System.out.println(array[i]);
        }
    }
}

### Задача: Напишите программу, которая выводит на консоль простые числа в промежутке от [2, 100]. Используйте для решения этой задачи оператор "%" (остаток от деления) и циклы.





public class lib  {
    public static void main(String[] args) {
        for (int i = 2; i <= 100; i++) {
            boolean isPrime = true;
            for (int j = 2; j < i; j++) {
                if (i % j == 0) {
                    isPrime = false;
                    break; 
                }
            }
            
            if (isPrime) {
                System.out.println(i);
            }
        }
    }
}
### Задача: Создайте класс, который описывает вектор (в трёхмерном пространстве).

У него должны быть:
конструктор с параметрами в виде списка координат x, y, z
метод, вычисляющий длину вектора. Корень можно посчитать с помощью Math.sqrt():
$\sqrt{x^2 + y^2 + z^2}$
метод, вычисляющий скалярное произведение:
$x_1x_2 + y_1y_2 + z_1z_2$
методы для суммы и разности:
$(x_1 + x_2, y_1 + y_2, z_1 + z_2)$
$(x_1 - x_2, y_1 - y_2, z_1 - z_2)$
статический метод, который принимает целое число N, и возвращает массив случайных векторов размером N.

public class lib {
    private double x;
    private double y;
    private double z;

    public lib(double x, double y, double z) {
        this.x = x;
        this.y = y;
        this.z = z;
    }

    public double length() {
        return Math.sqrt(x * x + y * y + z * z);
    }

    public double scalarProduct(lib vector) {
        return x * vector.x + y * vector.y + z * vector.z;
    }


    // Method to add two vectors
    public lib add(lib vector) {
        return new lib(
                x + vector.x,
                y + vector.y,
                z + vector.z
        );
    }

    public lib subtract(lib vector) {
        return new lib(
                x - vector.x,
                y - vector.y,
                z - vector.z
        );
    }
    
    public String toString() {
        return "Vector{" +
                "x=" + x +
                ", y=" + y +
                ", z=" + z +
                '}';
    }

    public static void main(String[] args) {
        // Predefined values
        lib vector1 = new lib(1.0, 2.0, 3.0);
        lib vector2 = new lib(4.0, 5.0, 6.0);

        // Printing vectors and their properties
        System.out.println("Vector 1: " + vector1);
        System.out.println("Vector 2: " + vector2);
        System.out.println("Length of Vector 1: " + vector1.length());
        System.out.println("Scalar product of Vector 1 and Vector 2: " + vector1.scalarProduct(vector2));
        System.out.println("Addition of Vector 1 and Vector 2: " + vector1.add(vector2));
        System.out.println("Subtraction of Vector 1 and Vector 2: " + vector1.subtract(vector2));
    }
}
### Задача:
### Задача:
### Задача:
### Задача:
### Задача:
### Задача:
### Задача:
