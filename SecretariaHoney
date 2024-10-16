
package enrollment;

import java.util.Scanner;


public class Enrollment {
      public void addStudent(){
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Student Enrollment ID: ");
        String s_enrollment_id= sc.next();
        
        System.out.print("Student Enrollment Date: ");
        String s_enrollment_date = sc.next();
        
        System.out.print("Student Status: ");
        String s_status = sc.next();
        
        
        System.out.print("Student Semester: ");
        String s_semester = sc.next();
       

        String sql = "INSERT INTO StudentInfo ( s_enrollment id, s_enrollment date, s_status, s_semester) VALUES (?, ?, ?)";
        config conf = new config();
        conf.addStudent(sql, s_enrollment_id, s_enrollment_date, s_status, s_semester);
    }
     public void viewStudent(){
   
        String cqry = "SELECT  s_enrollment_id, s_enrollment_date, s_status, s_semester FROM StudentInfo";
        String[] hrds = {"ID", "Enrollment ID", "Enrollment Date", "Status", "Semester"};
        String[] clmns = {"s_id", "s_enrollment date", "s_status", "s_semester"};
        config conf = new config();
        conf.viewStudent(cqry, hrds, clmns);
    }

     
     private void updateStudent(){
         Scanner sc = new Scanner(System.in);
         System.out.println("Enter New Student ID: ");
         int id = sc.nextInt();
         
         System.out.print("Enter New Enrollment Date: ");
         String s_student_id = sc.next();
         
         System.out.print("Enter New Status: ");
         String s_enrollment_status = sc.next();
         
         System.out.print("Enter New Student : ");
         String s_student = sc.next();
         
          System.out.print("Enter new Semester: ");
         String s_semester = sc.next();
         
         String qry = "UPDATE StudentInfo SET s_student_id = ?, s_enrollment_date = ?, s_status= ?, s_semester = ? WHERE s_id = ? ";
         config conf = new config();
         conf.updateStudent(qry, s_student_id, s_enrollment_date, s_enrollment_status,s_semester, id);
             
     }
      public void deleteStudent(){
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter Student ID to delete: ");
        int id = sc.nextInt();
        
        
         String sqlDelete = "DELETE FROM StudentInfo WHERE student_id = ?";
         config conf = new config();
         conf.deleteStudent(sqlDelete, id);
       

}


   
     
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);
       
          Enrollment student = new Enrollment (); 
        String response;
        
        do{
            System.out.println("1. Add:");
            System.out.println("2. View:");
            System.out.println("3. Update:");
            System.out.println("4. Delete:");
            System.out.println("5. Exit:");
            
            System.out.print("Enter Action: ");
            int action = sc.nextInt();
            
            switch (action){
                case 1:
                    student.addStudent();
                    
                    break;
                    
                case 2:
                   student.viewStudent();
                    break;
                    
                    case 3:
                   student.viewStudent();
                   student.updateStudent();
                    break;
                    
                    case 4:
                    student.viewStudent();
                    student.deleteStudent();
                    student.viewStudent();
                    break;
   
                    
                    case 5: 
                    System.out.println("Exiting...");
                        break;
                    default:
                        System.out.println("Invalid action. Please try again.");
            }
            
            System.out.print("Continue (yes/no): ");
            response = sc.next();
            
        } while(response.equalsIgnoreCase("yes"));
        System.out.println("Thank You See You Soon!");
        
    }
    
}
       
    
    
       
    
    

