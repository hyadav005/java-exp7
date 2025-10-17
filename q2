import java.util.*;
import java.util.stream.*;

class Student {
    String name;
    double marks;

    Student(String name, double marks) {
        this.name = name;
        this.marks = marks;
    }
}

public class part_b {
    public static void main(String[] args) {
        List<Student> list = Arrays.asList(
            new Student("Keshav", 85),
            new Student("Anurag", 62),
            new Student("Aman", 98),
            new Student("Devansh", 72)
        );

        List<String> names = list.stream()
            .filter(s -> s.marks > 75)
            .sorted((a, b) -> Double.compare(a.marks, b.marks))
            .map(s -> s.name)
            .collect(Collectors.toList());

        for(String name : names) {
            System.out.println(name);
        }
    }
}
