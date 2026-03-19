import java.util.ArrayList;
import java.util.Scanner;

class Student {
    String name;
    ArrayList<Integer> marks;

    Student(String name, ArrayList<Integer> marks) {
        this.name = name;
        this.marks = marks;
    }

    int getHighest() {
        int highest = marks.get(0);
        for (int mark : marks) {
            if (mark > highest) {
                highest = mark;
            }
        }
        return highest;
    }

    int getLowest() {
        int lowest = marks.get(0);
        for (int mark : marks) {
            if (mark < lowest) {
                lowest = mark;
            }
        }
        return lowest;
    }

    double getAverage() {
        int sum = 0;
        for (int mark : marks) {
            sum += mark;
        }
        return (double) sum / marks.size();
    }
}

public class StudentGradeManager {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        ArrayList<Student> students = new ArrayList<>();
        int choice;
System.out.println("\n===== Student Grade Manager =====");

        do {
        System.out.println("1. Add Student");
            System.out.println("2. Display Summary Report");
            System.out.println("3. Exit");
            System.out.print("Enter your choice: ");

            choice = sc.nextInt();
            sc.nextLine();

            switch (choice) {

                case 1:
                    System.out.print("Enter student name: ");
                    String name = sc.nextLine();

                    System.out.print("Enter number of subjects: ");
                    int subjects = sc.nextInt();

                    ArrayList<Integer> marks = new ArrayList<>();

                    for (int j = 0; j < subjects; j++) {
                        System.out.print("Enter mark for subject " + (j + 1) + ": ");
                        marks.add(sc.nextInt());
                    }

                    sc.nextLine();

                    students.add(new Student(name, marks));
                    System.out.println("Student added successfully!");
                    break;

                case 2:
    if (students.isEmpty()) {
        System.out.println("\nNo data available to display.");
    } else {
        System.out.println("\n----- Student Summary Report -----");

        for (Student s : students) {
            System.out.println("\nStudent Name: " + s.name);
            System.out.println("Marks: " + s.marks);
            System.out.println("Average: " + String.format("%.2f", s.getAverage()));
            System.out.println("Highest: " + s.getHighest());
            System.out.println("Lowest: " + s.getLowest());
        }
    }
    break;
                case 3:
                    System.out.println("Exiting program...");
                    break;

                default:
                    System.out.println("Invalid choice!");
            }

        } while (choice != 3);

        sc.close();
    }
}
