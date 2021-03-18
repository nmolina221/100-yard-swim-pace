# 100-yard-swim-pace
# (JAVA) User can input a swim yardage and time. Outputs the necessary 100 yard swim time required to reach yardage in applicable time.

import java.util.Scanner;
public class findSpeed {

	public static void main(String[] args) {
		Scanner scnr = new Scanner(System.in);

		int yardage;
		int yardsDiv100;
		int time;
		int minute;
		double seconds;
		double secondsConversion;
		
		System.out.println("Enter swim yardage: ");
		yardage = scnr.nextInt();
		
		System.out.println("Enter swim time in seconds: ");
		time = scnr.nextInt();
		
		yardsDiv100 = yardage / 100; //converts total yardage to number of 100 yard laps
		minute = (time / yardsDiv100) / 60;
		secondsConversion = (time / yardsDiv100); //converts to seconds per 100 yards 
		seconds = (((secondsConversion / 60) - minute) * 60); 
		
		System.out.printf("Your pace (100 yard swim time) is " + minute + " minute(s) and %.1f seconds.\n", seconds);
		
		

	}

}
