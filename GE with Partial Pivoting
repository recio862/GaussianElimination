import java.util.*;
import java.io.*;
/**
 *   Gaussian Elimination Algorithm with Partial Pivoting and Elimination
 *   Separated from Solving. Designed to take input from a user and display
 *   resulting matrix.
 *    
 *   Author: Renato John Recio
 *   Date: 12/18/2013
 *    
 */

public class GE_Algorithm
{
    static double matrix[][];

    /**
     * Main Driver
     */
    public static void main(String[] args)
    {
        int rows, cols;
        int row_cols[] = new int[2];
        initialize_matrix(row_cols);
        forward_elimination(row_cols[0], row_cols[1]);

    }

    public static int max_pivot_row(int k, int rows){
        double max_value = matrix[k][k];
        int max_row = k;
        for (int r = k; r < rows; r++){
            if (Math.abs(matrix[r][k]) > max_value){
            max_value = matrix[r][k];
            max_row = r;
            }
            
        }
        return max_row;
    }
    public static void forward_elimination(int rows, int cols){
        int pivot_row;
        for (int k = 0; k < rows; k++){
            pivot_row = max_pivot_row(k, rows);
            
            
            
        }
        
        
        
    }
    
    /**
     * Configure initial matrix using user input
     */
    public static void initialize_matrix(int row_cols[]){
        Scanner in = new Scanner(System.in);
        Scanner line_in;
        String line;
        int rows, cols;
        System.out.print("Please enter the number of rows: ");
        rows = in.nextInt();
        System.out.print("Please enter the number of columns: ");
        cols = in.nextInt();

        if (rows <= 0 || cols <= 0){
            System.out.println("This matrix is invalid, program will now exit.");
            System.exit(0);
        }

        row_cols[0] = rows;
        row_cols[1] = cols;
        matrix = new double[rows][cols];
        System.out.println("We now have a " + rows + "x" + cols +" matrix.");
        System.out.println();

        for (int r = 0; r < rows; r++){
            if (r != 0)   System.out.print("Now enter the data for row #" + (r + 1) + ": ");
            else System.out.print("Now enter the data for row #" + (r + 1) + 
                    "\nUse spaces as delimiters (ex. 2.53 5.33 9.25) : ");
            if (r == 0) line = in.nextLine();
            line = in.nextLine();
            line_in = new Scanner(line);
            for (int c = 0; c < cols; c++){
                matrix[r][c] = Double.parseDouble(line_in.next());

            }
        }      
        
        System.out.println("Here is the matrix.");
        print_matrix(rows, cols);
        System.out.println("\nIf this is correct, press 1. Otherwise, press any key to try again.");
        String repeat = in.next();
        if (Integer.parseInt(repeat) != 1) initialize_matrix(row_cols);
    }

    /**
     * Print the matrix
     */
    public static void print_matrix(int rows, int cols){
        for (int r = 0; r < rows; r++){
            System.out.println();
            for (int c = 0 ; c < cols; c++){
                System.out.print(matrix[r][c] + " ");

            }

        }
   
    }

}
