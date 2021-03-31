# Knowledge Database

## Goals: 
To provide a working system that will search only the things I add. With a single word or two, the system will scan the files and find anything relevant.

## Reason: 
To quickly aid in providing knowledge that other search engines fail in. 

<i>This will be specific to things only relevant to science, math, and engineering. </i>


import java.io.File;  // Import the File class
import java.io.FileNotFoundException;  // Import this class to handle errors
import java.util.Scanner; // Import the Scanner class to read text files

public class ReadFile {
  public static void main(String[] args) {
    try {
      File myObj = new File("filename.txt");
      Scanner myReader = new Scanner(myObj);
      while (myReader.hasNextLine()) {
        String data = myReader.nextLine();
        System.out.println(data);
      }
      myReader.close();
    } catch (FileNotFoundException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    }
  }
}
