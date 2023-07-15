# Assignment-1
public class ArrayRotation {
    public static int[] rotateArray(int[] arr, int rotationCount) {
        int length = arr.length;
        rotationCount = rotationCount % length; // Normalize rotation count

        // Create a new array to store the rotated elements
        int[] rotatedArray = new int[length];

        // Copy the rotated elements to the new array
        System.arraycopy(arr, length - rotationCount, rotatedArray, 0, rotationCount);
        System.arraycopy(arr, 0, rotatedArray, rotationCount, length - rotationCount);

        return rotatedArray;
    }

    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5};
        int rotationCount = 2;
        int[] rotated = rotateArray(array, rotationCount);
        for (int num : rotated) {
            System.out.print(num + " ");
        }
        // Output: 4 5 1 2 3
    }
}
