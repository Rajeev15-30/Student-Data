import java.util.Scanner;
public class Studentdata {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("enter total number of subject : ");
        int numsubject = sc.nextInt();
        int totalMarks = 0;
        for (int i = 1; i <= numsubject; i++) {
            System.out.println("enter marks for subject" + i + " : ");
            int marks = sc.nextInt();
            while (marks < 0 || marks > 100) {
                System.out.println(" invalid marks: please enter marks between 0 & 100");
                System.out.println("enter marks for subject" + i + " : ");
                marks = sc.nextInt();
            }
            totalMarks += marks;
        }
        System.out.println("student result : ");
        System.out.println("total marks obtain in all subject : " + totalMarks);
        int AveragePercentage = totalMarks / numsubject;
        System.out.println(" average percentage : " + AveragePercentage);
        if (AveragePercentage >= 90) {
            System.out.println(" A+ ");
        } else if (AveragePercentage >= 80) {
            System.out.println(" B+ ");
        } else if (AveragePercentage >= 70) {
            System.out.println(" C+ ");
        } else if (AveragePercentage >= 60) {
            System.out.println(" D+ ");
        } else if (AveragePercentage >= 50) {
            System.out.println(" D ");
        } else {
            System.out.println(" E ");
        }
    }
}
