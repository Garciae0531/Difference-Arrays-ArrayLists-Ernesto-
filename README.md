# Difference-Arrays-ArrayLists-Ernesto-
Week 3 Discussion Post
import java.util.ArrayList;
import java.util.List;
import java.util.Arrays;

/**
 * A program to demonstrate the conceptual and practical differences between
 * Java Arrays and ArrayLists.
 */
class DifferenceArraysArrayLists {

    public static void main(String[] args) {
        System.out.println("--- Demonstrating Java Array ---");

        // 1. Fixed Size: An array's size is set at creation and cannot be changed.
        String[] fixedArray = new String[3];
        fixedArray[0] = "Apple";
        fixedArray[1] = "Banana";
        fixedArray[2] = "Cherry";

        System.out.println("Initial array size: " + fixedArray.length);
        System.out.println("Elements: " + Arrays.toString(fixedArray));
        
        // This line would cause an ArrayIndexOutOfBoundsException because the array is full.
        // Uncomment the line below to see the error:
        // fixedArray[3] = "Date";

        // 2. Can store primitive types directly.
        int[] intArray = {1, 2, 3};
        System.out.println("Primitive int array: " + Arrays.toString(intArray));
        
        System.out.println("\n--- Demonstrating Java ArrayList ---");
        
        // 1. Dynamic Size: An ArrayList's size can grow or shrink as needed.
        // We use a List reference type for good practice.
        List<String> dynamicList = new ArrayList<>();
        
        dynamicList.add("Apple");
        dynamicList.add("Banana");
        System.out.println("ArrayList size after 2 elements: " + dynamicList.size());
        
        // We can add more elements without needing to resize manually.
        dynamicList.add("Cherry");
        dynamicList.add("Date");
        System.out.println("ArrayList size after adding more: " + dynamicList.size());
        System.out.println("Elements: " + dynamicList.toString());

        // We can also remove elements, and the size adjusts automatically.
        dynamicList.remove(1); // Removes "Banana"
        System.out.println("ArrayList size after removing an element: " + dynamicList.size());
        System.out.println("Elements: " + dynamicList.toString());
        
        // 2. Can only store objects (not primitives).
        // This is where generics are used, providing type safety.
        List<Integer> integerList = new ArrayList<>();
        integerList.add(10); // Auto-boxing converts int 10 to Integer object
        integerList.add(20);
        System.out.println("Object-based ArrayList: " + integerList.toString());
    }
}
