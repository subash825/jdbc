package project1;
import java.sql.*;
import java.util.Scanner;
 class myclass{
    public static void main(String args[]) {
        try{
            Scanner sc = new Scanner(System.in);
            Connection connect = DriverManager.getConnection("jdbc:mysql://localhost:3306/crime", "root", "tiger");
            Statement st = connect.createStatement();
            System.out.println("Database Configure:");
            System.out.println("Enter your choice:\n1.Update\n2.Delete\n3.Insert\n4.Show\nAny other choice to exit");
            int choice = sc.nextInt();
            while(choice == 1 || choice == 2 || choice ==3 || choice == 4) {
                switch(choice) {
                    case 1:
                        System.out.println("Choose the column you wish to update:\n1.no\n2.name\n3.place\n4.crime_date\n5.case_details\nAny other choice to complete your update");
                        int choice2 = sc.nextInt();
                        while (choice2 == 1 || choice2 == 2 || choice == 3) {
                            switch (choice2) {
                                case 1:
                                    System.out.println("Enter the value;");
                                    int a = sc.nextInt();
                                    System.out.println("Where you want to update(no)");
                                    int b = sc.nextInt();
                                    st.executeUpdate("update wantedlist set no = " + a + " where no = " + b);
                                    break;
                                case 2:
                                    System.out.println("Enter the value");
                                    sc.nextLine();
                                    String c = sc.nextLine();
                                    System.out.println("Where you want to update(no)");
                                    int d = sc.nextInt();
                                    st.executeUpdate("update wantedlist set name = '" + c + "' where no = " + d);
                                    break;
                                case 3:
                                    System.out.println("Enter the value;");
                                    sc.nextLine();
                                    String e = sc.nextLine();
                                    System.out.println("Where you wantedlist to update(no)");
                                    int f = sc.nextInt();
                                    st.executeUpdate("update wantedlist set  = '" + e + "' where no = " + f);
                                    break;
                            }
                            System.out.println("Updated Successfully");
                            System.out.println("Choose the column you wish to update:\n1.no\n2.name\n3.place\n4.crime_date\n5.case_details\nAny other choice to complete your update");
                            choice2 = sc.nextInt();
                        }
                        break;
                    case 2:
                        System.out.println("Enter the number of criminal you want to remove");
                        int x = sc.nextInt();
                        st.executeUpdate("delete from wantedlist where no = " + x);
                        System.out.println("Row Deleted Successfully");
                        break;
                    case 3:
                        System.out.println("Enter the number of criminal");
                        int no1 = sc.nextInt();
                        System.out.println("Enter the name of criminal");
                        sc.nextLine();
                        String name1 = sc.nextLine();
                        sc.nextLine();
                        String place1 = sc.nextLine();
                        sc.nextLine();
                        String crime_date1 = sc.nextLine();
                        sc.nextLine();
                        String case_details1 = sc.nextLine();
                        sc.nextLine();
                        String query = "insert into wantedlist (no, name, place,crime_date,case_details) values (" + no1 + ", '" + name1 + "','" + place1 + "' ,'"+ crime_date1 + "' , " + case_details1 + "')";
                        st.executeUpdate(query);
                        System.out.println("Successfully Inserted");
                        break;
                    case 4:
                        ResultSet rs = st.executeQuery("select * from wantedlist");
                        System.out.println("no    name        place    crime_date    case_details");
                        while(rs.next()) {
                        int no = rs.getInt("no");
                        String name = rs.getString("name");
                        String place = rs.getString("place");
                        String crime_date = rs.getString("crime_date");
                        String case_details = rs.getString("case_details");
                        System.out.println(no+ "      " + name + "        " + place + "      " + crime_date + "        " + case_details);
                        }
                        break;
                }
                System.out.println("Enter your choice:\n1.Update\n2.Delete\n3.Insert\n4.Show\nAny other choice to exit");
                choice = sc.nextInt();
            }
            connect.close();
            st.close();
        }
        catch (Exception e) {
            System.out.println(e.toString());
        }
    }
}
