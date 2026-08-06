import java.util.Scanner;
import java.util.ArrayList;
public class SSMS {
	public static void main(String[] args) {
		try(Scanner sc = new Scanner(System.in)) {
			ArrayList<String> view = new ArrayList<>();
			ArrayList<String> menu = new ArrayList<>();
			ArrayList<String> Id = new ArrayList<>();
			ArrayList<String> course = new ArrayList<>();
      ArrayList<String> gender = new ArrayList<>();
			ArrayList<String> courselect = new ArrayList<>();
      ArrayList<Integer> age = new ArrayList<>();

	 		menu.add("1. Add Student");
			menu.add("2. View Student");
			menu.add("3. Search Student");
			menu.add("4. Delete Student");
			menu.add("5. Clear All Student");
			menu.add("6. Exit Program");

			while (true) {
				System.out.println("\n ------- Student Management System --------");
				for (String list : menu) {
					System.out.println(list);
				}
				 System.out.print("Enter Your choice:");
				 int choice = sc.nextInt();
				 sc.nextLine();

				switch (choice) {
				    case 1:
					while (true) {
					System.out.println("\nID Format Example:(2025-0115-K");
					System.out.print("Enter Student ID: ");
					String studentID = sc.nextLine();

					if (studentID.matches("\\d{4}-\\d{4}-[A-Z]")) {
						Id.add(studentID);
						break;
					} else {
					  System.out.println("\nInvalid Student ID!");
					  System.out.println("Format should be: 2025-0115-K");
					continue;
					  }
					}
					 System.out.print("\nEnter Complete Name:");
					 String name = sc.nextLine();

					 if (name.isEmpty()) {
						System.out.println("Name must not Empty!");
						 continue;
					} else if (!name.matches("[a-zA-Z ]+")) {
						 System.out.println("Error: Name must not contain any especial symbol!");
						 continue;
				    }
              view.add(name);
              System.out.println("Student Name Added Successfully!");
               
               System.out.print("\nEnter Student Age: ");
               while(!sc.hasNextInt()){
                System.out.println("Enter Numbers only Please try again!");
                sc.nextLine();
               }
               int ages = sc.nextInt();
                if(ages <= 10 && ages >= 55 ){
                   System.out.println("Invalid age Please try again!");
                   continue;
               }else{
		               age.add(ages);
                   System.out.println("Age added Successfully");
                }
               

               
               

		        while (true){
                     System.out.println("\n------------ Select A Gender ------------");
                     System.out.println("MALE = (M|m) || FEMALE = (F|f):");
                     System.out.print("Enter Your Gender:");
                     char gend = sc.next().charAt(0);

                     switch(gend){
                     case 'M':
					 case 'm':
                     String M = "MALE";
                     gender.add(M);
                     System.out.println("Gender added Successfully!");
                     break;
                     case 'F':
					 case 'f':
                     String F = "FEMALE";
                     gender.add(F);
                     System.out.println("Gender Added Successfully!");
                     break;
                     default:
                      System.out.println("Invalid choice! Please Try again!");
					  continue;
                   }
				 
				

					courselect.add("\n------------------ SELECT A COURSE -------------------");
					courselect.add("---------------TECHNOLOGY & COMPUTING --------------");
					courselect.add("1. Bachelor of Science in Computer Science (BSCS)");
					courselect.add("2. Bachelor of Science in Information Technology (BSIT)");
					courselect.add("3. Bachelor of Science in Information Systems (BSIS)");
					courselect.add("4. Bachelor of Science in Cybersecurity (BSC)");

					courselect.add("\n------------------- ENGINEERING -------------------");
					courselect.add("5. Bachelor of Science in Civil Engineering (BSCE)");
					courselect.add("6. Bachelor of Science in Mechanical Engineering (BSME)");
					courselect.add("7. Bachelor of Science in Electrical Engineering (BSEE)");
					courselect.add("8. Bachelor of Science in Computer Engineering (BSCpE)");

					courselect.add("\n----------------- BUSINESS & MANAGEMENT -----------------");
					courselect.add("10. Bachelor of Science in Business Administration (BSBA)");
					courselect.add("11. Bachelor of Science in Accountancy (BSA)");
					courselect.add("12. Bachelor of Science in Hospitality Management (BSHM)");

					courselect.add("\n----------------- TEACHER EDUCATION -----------------");
					courselect.add("13. Bachelor of Elementary Education (BEEd)");
					courselect.add("14. Bachelor of Secondary Education (BSEd)");
					courselect.add("15. Bachelor of Physical Education (BPEd)");
					courselect.add("16. Bachelor of Early Childhood Education (BECEd)");

					courselect.add("\n----------------- AGRICULTURE -----------------");
					courselect.add("16. Bachelor of Science in Agriculture (BSA)");
					courselect.add("17. Bachelor of Science in Agribusiness");
					courselect.add("18. Bachelor of Science in Forestry");


					for (String c : courselect) {
						System.out.println(c);
					}

					System.out.print("\nSelect Course by number: ");
					while (!sc.hasNextInt()) {
						System.out.println("Select by number Only Please Try again!");
						System.out.print("\nSelect Course by number only:");
						sc.nextLine();
						continue;
					}
					int select = sc.nextInt();

					if (select >= 1 && select <= 18) {
						System.out.println("Course Added Successfully!");

						for (String c : courselect) {
							if (c.startsWith(select + ".")) {
								course.add(c);
								break;
							}
						}

					 } else {
						System.out.println("Invalid Course Number!");
					 }
					 
					 break;
					 
					 }
					 break;
				case 2:
					if (view.isEmpty()) {
						System.out.println("\nNo Student yet");
					} else {
						System.out.println("\n ------ Student List! ------");
						System.out.println(" Total Student: " + view.size());
						for (int i = 0; i < view.size(); i++) {
							String format = String.format(" |ID: %-10s\n |Name: %-15s\n |Age: %2d \n |Gender: %-15s \n |Course: %-15s", Id.get(i), view.get(i), age.get(i), gender.get(i), course.get(i) + "\n");
							System.out.println(format);
						}
					  }
					 break;
					
				case 3:
					System.out.print("\nEnter Student ID number to search: ");
					String search = sc.nextLine();
					boolean found = false;

					for (int i = 0; i < Id.size(); i++) {
						if (Id.get(i).equals(search)) {
							System.out.println("\n-------- Student Found --------");
							System.out.println("ID: " + Id.get(i));
							System.out.println("Name: " + view.get(i));
              System.out.println("Age: "+ age.get(i));
							System.out.println("Gender: "+ gender.get(i));
							System.out.println("Course: " + course.get(i));
							found = true;
							break;
						}
					}

					if (!found) {
						System.out.println("\nStudent not Found!");
					}
					break;
				case 4:
					System.out.print("\nEnter Student ID number to Delete:");
					String delete = sc.nextLine();
					boolean deleted = false;

					for (int i = 0; i < Id.size(); i++) {
						if (Id.get(i).equalsIgnoreCase(delete)) {
							System.out.println("\n ID: " +  Id.get(i) + "\n|Name: " +  view.get(i) + "\n|Age: "+ age.get(i) + "\n|Gender: " + gender.get(i) + "\n|Course:  " + course.get(i) + "\n Successfully Deleted!");
							Id.remove(i);
							view.remove(i);
              age.remove(i);
							gender.remove(i);
							course.remove(i);
							deleted = true;
							break;
						}
					}
					if (!deleted) {
						System.out.println("\nStudent not Found!");
					}
					break;
				case 5:
					System.out.print("Are you sure you want to clear all Student? (y|n):");
					String clear = sc.nextLine();
				             
					if (clear.equalsIgnoreCase("y")) {
				    if(view.isEmpty() && Id.isEmpty() && age.isEmpty() && gender.isEmpty() && course.isEmpty()){
				       System.out.println("No student yet!");
				           break;
				       }else{
				       }
						view.clear();
						Id.clear();
            age.clear();
						gender.clear();
						course.clear();
						System.out.println("\nAll Student has been cleared!");
					    
					  	 }else{
							System.out.println("\nBack to Homepage....");
							break;
					  	 }
						break;
					 case 6:
						System.out.println("\nThank you for using this App!");
						return;
					 default:
						System.out.println("Invalid Choice Please try again!");
					}
			
			
				}
			}
		}
	}
