[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MNuUGPL5)
import java.util.ArrayList; 
import java.util.Scanner; 
public class StringListOperations { 
 
 private static ArrayList<String> list = new ArrayList<>(); 
 public static void insertItem(String item) { 
 list.add(item); 
 } 
 public static void deleteItem(String item) { 
 if (list.contains(item)) { 
 list.remove(item); 
 System.out.println(item + " has been removed."); 
 } else { 
 System.out.println(item + " not found in the list."); 
 } 
 } 
 public static void displayList() { 
 if (list.isEmpty()) { 
 System.out.println("The list is empty."); 
 } else { 
 System.out.println("List items: " + list); 
 } 
 } 
 public static void searchItem(String item) { 
 if (list.contains(item)) { 
 System.out.println(item + " is found in the list."); 
 } else { 
 System.out.println(item + " is not found in the list."); 
 } 
 } 
 public static void main(String[] args) { 
 Scanner sc = new Scanner(System.in); 
 int choice; 
 do { 
 System.out.println("\nSelect an operation:"); 
 System.out.println("1. Insert Item"); 
 System.out.println("2. Delete Item"); 
 System.out.println("3. Display List"); 
 System.out.println("4. Search Item"); 
 System.out.println("5. Exit"); 
 choice = sc.nextInt(); 
 sc.nextLine(); 
 switch (choice) { 
 case 1: 
 System.out.print("Enter item to insert: "); 
 String insertItem = sc.nextLine(); 
 insertItem(insertItem); 
 break; 
 case 2: 
 System.out.print("Enter item to delete: "); 
 String deleteItem = sc.nextLine(); 
 deleteItem(deleteItem); 
 break; 
 case 3: 
 displayList(); 
 break; 
 case 4: 
 System.out.print("Enter item to search: "); 
 String searchItem = sc.nextLine(); 
 searchItem(searchItem); 
 break; 
 case 5:
 System.out.println("Exiting program."); 
 break; 
 default: 
 System.out.println("Invalid choice! Please choose a valid option."); 
 } 
 } while (choice != 5); 
 sc.close(); 
 } 
}
