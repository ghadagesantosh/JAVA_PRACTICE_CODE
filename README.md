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
_______________________________________________________________________________________________________________________________________________________

String Revese Program

// Online Java Compiler
// Use this editor to write, compile and run your Java code online

class Main {
    public static void main(String[] args) {
        
        String s="MADAM";
        String rev="";
        
        char a[]=s.toCharArray();
        
        for (int i=a.length-1; i>=0;i--)
        {
            rev=rev+a[i];
            System.out.println(a[i]); //printing array
        }
        
        
        System.out.println(rev);// printing reverse char array
    }
}
_______________________________________________________________________________________________________________________________________________________

StringBuffer.

// Online Java Compiler
// Use this editor to write, compile and run your Java code online

class Main {
    public static void main(String[] args) {
        String s= "Avadhut";
        StringBuffer sb = new StringBuffer(s);
        System.out.println(sb.append("vaddikar"));
    }
}
_______________________________________________________________________________________________________________________________________________________

Given String is palindrome or not.

class Main {
    public static void main(String[] args) {
        
        String s="MADAM";
        String rev="";
        

        for (int i=s.length()-1; i>=0;i--)
        {
            rev=rev+ s.charAt(i);
        }
        
        if (s.equals(rev))
        {
            System.out.println("Given String is palindrome");
        }
        
        else 
        {
         System.out.println("Given String is not palindrome");

        }
        
       
    }
}

_______________________________________________________________________________________________________________________________________________________
// Online Java Compiler
// Use this editor to write, compile and run your Java code online

class Main {
    public static void main(String[] args) {
        
        String s="wel&&%%^^())*come";
        String z=s.replaceAll("[^a-zA-Z0-9]", "");
        System.out.println(z);
    }
}
-----------------------------------------------------------------------------------------------
//Write a Java program to find the number of even and odd integers in a given array of integers.
public class Main
{
	public static void main(String[] args) {
		
		int arr[]={1,2,3,4,5,6};
		
		Arrays.sort(arr);
		
		for(int i=0;i<arr.length;i++)
		{
		    if(arr[i]%2==0)
		    {
		        System.out.println("EVEN NUMBER"+arr[i]);
		    }
		    else
		    {
		        System.out.println("ODD NUMBER"+arr[i]);
		    }
}
-------------------------------------------------------------------------
//Write a Java program to get the difference between the largest and smallest values in an array of integers.

public class Main
{
	public static void main(String[] args) {
		
		int arr[]={1,21,11,42,5,6};
		
		Arrays.sort(arr);
		
		int small= arr[0];
		int large=arr[(arr.length-1)];
		
		System.out.println("Small Number"  +small);
        System.out.println("Large Number"  +large);
        
        int diff=large-small;
        
        System.out.println("Diff bet large and small     "  +diff);
		
----------_---------------------------------------------------------------------------
		
		//Find third largest number from given array
public class Bike1 {
	
	public static void main (String [] args)
	{

		int a[]= {6,4,2,3,5,1,9,8,7};
		Arrays.sort(a);
		System.out.println(a.length-2);
	
		
	
	}  
	}
-------------------------------------------------------------------------

Write a Java program to iterate a linked list in reverse order.


import java.util.*;
import java.util.LinkedList;
import java.util.Iterator;

public class Main
{
	public static void main(String[] args) {
 // create an empty linked list
     LinkedList<String> l_list = new LinkedList<String>();
   // use add() method to add values in the linked list
          l_list.add("Red");
          l_list.add("Green");
          l_list.add("Black");
          l_list.add("Pink");
          l_list.add("orange");
      
        // print original list
   System.out.println("Original linked list:" + l_list);  
 
    Iterator it = l_list.descendingIterator();

     // Print list elements in reverse order
     System.out.println("Elements in Reverse Order:");
     while (it.hasNext()) {
        System.out.println(it.next());
     }
  }
}
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Occurance of characters in given String


import java.util.*;
class Main {
    public static void main(String[] args) {
        String s= "HANAMANT BOODI";
        
        char array[] = s.toCharArray();
        
LinkedHashMap<Character, Integer> map = new LinkedHashMap<Character, Integer>();

     for (char c : array) {
            if (!map.containsKey(c)) {
 
              
                map.put(c,1);
            }
            else{
                int n= map.get(c);
                map.put(c, n+1);
            }
     }
        System.out.println(map);
    }
}


