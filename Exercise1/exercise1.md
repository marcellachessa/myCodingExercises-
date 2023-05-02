import java.util.Random;

// Bubble sort starts from the beginning of the list, compare every adjacent
// pair, swap their position if they are not in the right order until it stops at when numbers are in order.

// Quadratic time O(n^2)
// small data set = okay-ish
// large data set = BAD (plz don't)

public class BubbleSort {
public static void main(String[] args) {
        int array[] = {9, 1, 8, 2, 7, 3, 6, 4, 5, 10, 11, 90, 67, 88};  // array of unsorted integers 
        bubbleSort(array);              // bubble sort method  , (array) is the argument

        for (int i : array) {
            System.out.print(i);
        }
    }
    public static void bubbleSort(int array[]) {                   // nested for loop to define bubble sort method
        for(int i = 0; i < array.length - 1; i++) {                // outer loop of the bubbleSort method iterates through the entire array length - 1 times. This is because the largest element is guaranteed to "bubble up" to the end of the array after the first pass, and so on.
            for(int j = 0; j < array.length - i - 1; j++) {       // The inner loop of the bubbleSort method compares adjacent pairs of elements in the array and swaps them if they are not in order. This loop runs array.length - i - 1 times on each iteration of the outer loop. The reason for subtracting i is because the last i elements of the array are already sorted.brb
                if(array[j] > array[j+1]) {
                    int temp = array[j];        // assistance of a temp variable to swap number
                    array[j] = array[j+1];     
                    array[j+1] = temp;
                }
            }
        }
        
    }
}
