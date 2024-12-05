# JAVA_PRACTICE_CODE for Interview

//how to find all duplicate characters in a string using nested for loop.

public class Duplicates {
	   public static void main(String argu[]) {
	      String str = "beautiful sea";
	      char[] carray = str.toCharArray();
	      System.out.println("The string is: " + str);
	      System.out.print("Duplicate Characters in above string are: ");
		  // nested for loop to print duplicate characters
	      for (int i = 0; i < str.length(); i++) {
	         for (int j = i + 1; j < str.length(); j++) {
	            if (carray[i] == carray[j]) {
	               System.out.print(carray[j] + " ");
	               break;
	            }
	         }
	      }
	   }
	}
