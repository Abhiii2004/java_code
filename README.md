//Rock,Paper & Scissors
# package com.company;

import java.util.Random;
import java.util.Scanner;

public class rockPaperScissors{

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Random rand = new Random();

        String[] options= {"rock", "paper", "scissors"};
        String userChoice, computerChoice;

        while (true) {
            System.out.println("\n enter rock,paper,or scissors(or type exit to quit)");
            userChoice = sc.next().toLowerCase();
            if(userChoice.equals("exit"))
            {
                System.out.println("thank you");
                break;}
            if (!userChoice.equals("rock") && !userChoice.equals("paper") && !userChoice.equals("scissors"))
            {
                System.out.println("Invalid input! try again");
                continue;
            }
            computerChoice = options [rand.nextInt(3)];
            System.out.println("computer choice " + computerChoice);
            if (userChoice.equals(computerChoice)) {
                System.out.println("its a tie");
            } else if (
                    userChoice.equals("rock") && computerChoice.equals("scissors") ||
                            userChoice.equals("paper") && computerChoice.equals("rock") ||
                            userChoice.equals("scissors") && computerChoice.equals("paper")) {
                System.out.println("you win!");
            } else {
                System.out.println("computer wins!");
            }}
            sc.close();
    }}
