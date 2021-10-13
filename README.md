# function1
package com.company;
import java.util.Scanner;
import java.util.Random;
public class Main {

    public static void main(String[] args) {
        Random r = new Random();
        Scanner sc = new Scanner(System.in);
        int n, m;
        System.out.println("Zhol:");
        n = sc.nextInt();
        System.out.println("Bagany:");
        m = sc.nextInt();
        int a[][] = new int[n][m];

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                a[i][j] = r.nextInt(20) - 10;
                System.out.print(a[i][j] + "\t");
            }
            System.out.println();
        }

        int min;
        int min1;
        min = a[0][0];
        min1 = a[n-1][m-1];
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                if (min > a[i][j]) {
                    min = a[i][j];}
                    if (a[i][j] != min && min1 > a[i][j])
                        min1 = a[i][j];

            }
        }


        System.out.println("min :" + min);
        System.out.println("min1 : " + min1);

    }}

