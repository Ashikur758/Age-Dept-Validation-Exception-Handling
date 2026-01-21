import java.util.Scanner;

class AgeException extends Exception {
    AgeException(String message) {
        super(message);
    }
}

class DepartmentException extends Exception {
    DepartmentException(String message) {
        super(message);
    }
}

public class AgeDeptValidation {

    static void checkAge(int age) throws AgeException {
        if (age < 18 || age > 60) {
            throw new AgeException("Invalid age");
        }
    }

    static void checkDepartment(String dept) throws DepartmentException {
        if (!(dept.equalsIgnoreCase("CSE") ||
              dept.equalsIgnoreCase("EEE") ||
              dept.equalsIgnoreCase("ICT"))) {
            throw new DepartmentException("Invalid department");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Enter age: ");
            int age = sc.nextInt();
            sc.nextLine(); // consume newline

            System.out.print("Enter department: ");
            String dept = sc.nextLine();

            checkAge(age);
            checkDepartment(dept);

            System.out.println("Validation Successful");
        } 
        catch (AgeException | DepartmentException e) {
            System.out.println(e.getMessage());
        }

        sc.close();
    }
}
