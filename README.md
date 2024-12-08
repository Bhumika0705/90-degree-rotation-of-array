# 90-degree-rotation-of-array
It will rotate you array by 90 degree
public class NinteyDegreerotate {
    public NinteyDegreerotate() {
    }

    public static void roatate(int[][] arr, int n) {
        for(int i = 0; i < n / 2; ++i) {
            for(int j = i; j < n - i - 1; ++j) {
                int temp = arr[i][j];
                arr[i][j] = arr[n - 1 - j][i];
                arr[n - 1 - j][i] = arr[n - 1 - i][n - 1 - j];
                arr[n - 1 - i][n - 1 - j] = arr[j][n - 1 - i];
                arr[j][n - 1 - i] = temp;
            }
        }

    }

    public static void main(String[] args) {
        int[][] arr1 = new int[][]{{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
        int n = 3;
        roatate(arr1, 3);

        for(int i = 0; i < n; ++i) {
            for(int j = 0; j < n; ++j) {
                System.out.print(arr1[i][j] + " ");
            }

            System.out.println();
        }

    }
}
