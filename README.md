# JAVA-ENUM-PRACTICE-WITH-MONTHS
This is a very simple way to incorporate enums with your Java code using months, souts, a switch statement, try/catch, and a scanner. This will help you begin your journey with enum


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

package com.Williford;


import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		Calender a = new Calender();
		Scanner scnr = new Scanner(System.in);

		System.out.println("Please enter the day of the month");

		Integer days = Integer.parseInt(scnr.nextLine());

		a.setDays(days);

		System.out.println("Please enter the year in a 4 digit format");

		Integer year = Integer.parseInt(scnr.nextLine());

		a.setYear(year);

		System.out.println("Please type in the month in a 2 digit format: ");
		try {
			switch (scnr.nextLine()) {
				case "01":
					System.out.println(Calender.Months.January + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "02":
					System.out.println(Calender.Months.February + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "03":
					System.out.println(Calender.Months.March + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "04":
					System.out.println(Calender.Months.April + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "05":
					System.out.println(Calender.Months.May + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "06":
					System.out.println(Calender.Months.June + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "07":
					System.out.println(Calender.Months.July + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "08":
					System.out.println(Calender.Months.August + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "09":
					System.out.println(Calender.Months.September + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "10":
					System.out.println(Calender.Months.October + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "11":
					System.out.println(Calender.Months.November + "/" + a.getDays() + "/" + a.getYear());
					break;
				case "12":
					System.out.println(Calender.Months.December + "/" + a.getDays() + "/" + a.getYear());
					break;


			}


		} catch(Exception error) {
			System.out.println("An Error has occurred: Exception " + error.getMessage() + "has been reached");

		}
	}
}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

package com.Williford;

public class Calender {
    enum Months { January, February, March, April, May, June, July,
                   August, September, October, November, December;
        @Override
        public String toString() {
            return super.toString();
        }
    }
    Integer days;
    Integer year;

    public Integer getDays() {
        return days;
    }

    public void setDays(Integer days) {
        this.days = days;
    }

    public Integer getYear() {
        return year;
    }

   public void setYear(Integer year){
        this.year = year;
   }
}
