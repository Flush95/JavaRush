package com.javarush.test.level14.lesson08.bonus02;

/* НОД
Наибольший общий делитель (НОД).
Ввести с клавиатуры 2 целых положительных числа.
Вывести в консоль наибольший общий делитель.
*/

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.List;

public class Solution
{
    public static void main(String[] args) throws Exception
    {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int firstNumber = Integer.parseInt(reader.readLine());
        int secondNumber = Integer.parseInt(reader.readLine());

        List<Integer> firstNumberDividers = new ArrayList<>();
        List<Integer> secondNumberDividers = new ArrayList<>();

        fillDividersList(firstNumberDividers, firstNumber);
        fillDividersList(secondNumberDividers, secondNumber);

        int number = 0;
        for (int i = firstNumberDividers.size() - 1; i >= 0 ; i--) {
            for (int j = secondNumberDividers.size() - 1; j >= 0; j--) {
                if (firstNumberDividers.get(i) == secondNumberDividers.get(j)) {
                    number = firstNumberDividers.get(i);
                    break;
                }
            }
            if (number != 0) break;
        }
        System.out.println(number);
    }
    public static void fillDividersList (List<Integer> list, int number) {
        for (int i = 1; i <= number; i++) {
            if (number % i == 0)
                list.add(i);
        }
    }

}
