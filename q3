import java.util.*;
import java.util.stream.*;

class Product {
    String name;
    double price;
    String category;

    Product(String name, double price, String category) {
        this.name = name;
        this.price = price;
        this.category = category;
    }
}

public class part_c {
    public static void main(String[] args) {
        List<Product> list = Arrays.asList(
            new Product("Laptop", 90000, "Electronics"),
            new Product("Phone", 60000, "Electronics"),
            new Product("Shirt", 1500, "Apparel"),
            new Product("Jeans", 2500, "Apparel"),
            new Product("Book", 500, "Stationery")
        );

        // Group products by category (readable output)
        Map<String, List<Product>> byCategory = list.stream()
            .collect(Collectors.groupingBy(p -> p.category));

        System.out.println("Products grouped by category:");
        for(String cat : byCategory.keySet()) {
            System.out.println(cat + ":");
            for(Product p : byCategory.get(cat)) {
                System.out.println("  " + p.name);
            }
        }
        System.out.println();

        // Most expensive product in each category
        Map<String, Optional<Product>> maxProduct = list.stream()
            .collect(Collectors.groupingBy(
                p -> p.category,
                Collectors.maxBy(Comparator.comparingDouble(p -> p.price))
            ));

        System.out.println("Most expensive product in each category:");
        for(String cat : maxProduct.keySet()) {
            Product p = maxProduct.get(cat).orElse(null);
            if(p != null) {
                System.out.println(cat + ": " + p.name + " " + p.price);
            }
        }
        System.out.println();

        // Average price
        double avg = list.stream()
            .mapToDouble(p -> p.price)
            .average()
            .orElse(0);

        System.out.println("Average price of all products: " + avg);
    }
}
