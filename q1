import java.util.*;

class Employee {
    String name;
    int age;
    double salary;

    Employee(String name, int age, double salary) {
        this.name = name;
        this.age = age;
        this.salary = salary;
    }
}

public class part_a {
    public static void main(String[] args) {
        List<Employee> list = new ArrayList<>();
        list.add(new Employee("Ankit", 25, 35000.0));
        list.add(new Employee("Sneha", 30, 40000.0));
        list.add(new Employee("Raj", 22, 50000.0));

        // Sort by name
        list.sort((a, b) -> a.name.compareTo(b.name));
        for(Employee e : list) {
            System.out.println(e.name + " " + e.age + " " + e.salary);
        }
        System.out.println();

        // Sort by age
        list.sort((a, b) -> a.age - b.age);
        for(Employee e : list) {
            System.out.println(e.name + " " + e.age + " " + e.salary);
        }
        System.out.println();

        // Sort by salary descending
        list.sort((a, b) -> Double.compare(b.salary, a.salary));
        for(Employee e : list) {
            System.out.println(e.name + " " + e.age + " " + e.salary);
        }
    }
}
