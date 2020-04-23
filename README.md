# Pemrograman-Berorientasi-Obyek4
Source Code JAVA dari Class Diagram Course, Instructor dan Textbook

Class Course
public class Course
{
   private String courseName;      // Name of the course
   private Instructor instructor;  // The instructor
   private TextBook textBook;         


   public Course(String name, Instructor instr,
                 TextBook text)
   {
      // Assign the courseName.
      courseName = name;
      
      // Create a new Instructor object, passing
      // instr as an argument to the copy constructor.
      instructor = instr;

      // Create a new TextBook object, passing
      // text as an argument to the copy constructor.
      textBook = text;
   }

   /**
    * getName method
    */
   
   public String getName()
   {
      return courseName;
   }
   
   /**
    * getInstructor method
    */
   
   public Instructor getInstructor()
   {
      // Return a copy of the instructor object.
      return instructor;
   }

   /**
    * getTextBook method 
    */
   
   public TextBook getTextBook()
   {
      // Return a copy of the textBook object.
      return textBook;
   }
   
 /**
    * The toString method returns a string containing 
    * the course information.
    */

   public String toString()
   {
      // Create a string representing the object.
      String str = "Course name: " + courseName
                   + "\nInstructor Information:\n"
                   + instructor
                   + "\nTextbook Information:\n"
                   + textBook;

      // Return the string.
      return str;
   }
}

Class CourseDemo
public class CourseDemo
{
   public static void main(String[] args)
   {
      // Create an Instructor object.
      Instructor myInstructor =
          new Instructor("Shibghotur", "Ayu", "18051214068");
      
      // Create a TextBook object.
      TextBook myTextBook =
          new TextBook("Rantau 1 Muara",
                       "A. Fuadi", "Gramedia");
                       
      // Create a Course object.
      Course myCourse = 
         new Course("Pemrograman Berorientasi Obyek", myInstructor,
                    myTextBook);
      
      // Display the course information.
      System.out.println(myCourse);
   }
}

Class TextBook
public class TextBook
{
   private String title,     // Title of the book
                  author,    // Author's last name
                  publisher; // Name of publisher

   /**
    * This constructor accepts arguments for the   
    * title, author, and publisher.
    */

   public TextBook(String textTitle, String auth,
                   String pub)
   {
      title = textTitle;
      author = auth;
      publisher = pub;
   }
 /**
    * The toString method returns a string containing 
    * the textbook information. 
    */

   public String toString()
   {
      // Create a string representing the object.
      String str = "Title: " + title
                   + "\nAuthor: " + author
                   + "\nPublisher: " + publisher;

      // Return the string.
      return str;
   }
}

Class Instructor
public class Instructor
{
   private String lastName,     // Last name   
                  firstName,    // First name
                  officeNumber; // Office number

   /**
    * This constructor accepts arguments for the   
    * last name, first name, and office number.
    */

   public Instructor(String lname, String fname,
                     String office)
   {
      lastName = lname;
      firstName = fname;
      officeNumber = office;
   }

   

   /**
    * The set method sets each field. 
    */
   
   public void set(String lname, String fname,
                   String office)
   {
      lastName = lname;
      firstName = fname;
      officeNumber = office;
   }
   
   /**
    * The toString method returns a string containing 
    * the instructor information.
    */

   public String toString()
   {
      // Create a string representing the object.
      String str = "Last Name: " + lastName
                   + "\nFirst Name: " + firstName
                   + "\nOffice Number: " + officeNumber;

      // Return the string.
      return str;
   }
} 

 
