#Day 2
Q1:Write a program to find the sum of the elements present inside the array.
import java.util.Scanner;
public class Main {

    public static void main(String[] args) {
       Scanner input = new Scanner(System.in);
        int size = input.nextInt();  
        int[] arr = new int[size];
         // read the array elements
        for (int i = 0; i < size; i++) {
            arr[i] = input.nextInt();
        }
        
        sumArray(arr,size);
        
    }
    
    public static void sumArray(int[] arr,int size)
    {
      //write logic here and display sum
      int sum =0;
      for(int i=0;i<size;i++){
          sum+=arr[i];
      }
      System.out.print("the sum of the elements in the array = " + sum);
     
    }
}
Q2:Write a program that takes the row & columns input from the user to populate a 2D array and then prints the array.
import java.util.Scanner;

public class MultidimensionalArrayExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // TODO: Write your code here
        int rows=scanner.nextInt();
        int cols=scanner.nextInt();
        int [][] arr = new int[rows][cols];
        for (int i=0;i<rows;i++){
            for(int j =0;j<cols;j++){
                arr[i][j]=scanner.nextInt();
            }

        }
        for(int i=0;i<rows;i++){
            for(int j=0;j<cols;j++){
                System.out.print(arr[i][j] + " ");
            }
            System.out.println();
        }
        
        
        scanner.close();
    }
}
  Q3:Write a function to reverse each word in a string.

Description :- A method has to be created that takes a string as input and extracts each word from that string and then reverse each word individually and gives the output as a reversed string. 
import java.util.Scanner;
public class Main {

    public static void main(String[] args) {

        //write your answer here
        Scanner sc = new Scanner(System.in);
        String input = sc.next();
        input+=sc.nextLine();
        String[] words = input.split(" ");
        for(int i = 0;i<words.length;i++){
            StringBuilder sb = new
        StringBuilder(words[i]);
        words[i]=sb.reverse().toString();
        }
        for(int i =0; i<words.length;i++)
        {
            System.out.print(words[i]);
            if(i!=words.length-1)
        System.out.print(" ");
        }
    }
}
Q4:Equal character in string
You are given a string s. In one move you can change any character to another character.

You have to make a string which consists of the same character. Find the minimum move to do this task.
import java.util.Scanner;
public class Main {

    public static void main(String[] args) {

        //write your answer here
        Scanner sc = new Scanner(System.in);
        String S = sc.nextLine();
        int[] freq = new int[26];
        for(int i = 0; i < S.length(); i++){
            freq[S.charAt(i) - 'a']++;
        }
        int maxFreq=0;
        for(int i=0; i < 26; i++){
            if(freq[i]>maxFreq){
                maxFreq=freq[i];
            }
        }
        System.out.println(S.length()-maxFreq);
    }
}
