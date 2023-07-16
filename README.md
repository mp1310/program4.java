# program4.java
# Calculates the total count of number

import java.util.HashMap;
import java.util.Map;

public class NumberCount {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 8, 9, 12, 46, 76, 82, 15, 20, 30};

        // Initialize the count dictionary
        Map<Integer, Integer> countMap = new HashMap<>();
        for (int i = 1; i <= 9; i++) {
            countMap.put(i, 0);
        }

        // Count the numbers
        for (int number : numbers) {
            for (int i = 1; i <= 9; i++) {
                if (number % i == 0) {
                    countMap.put(i, countMap.get(i) + 1);
                }
            }
        }

        System.out.println("Output: " + countMap);
    }
}
