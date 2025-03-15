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


++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
JsonSchemaValidator

RestAssured.baseURI("");

String Response = RestAssured.given().log().all().header().body()
.when().post("resouce")
.then().aseertThat().log().all().statuscode(200)
.extract().response().asstring()
.body("courses[0]",equalsTo("java"))
.body("courses[1]",equalsTo("C") )
.body("name", equalsTo("scot")).log().all()
.header("Content-Type","application/json; charset-utf-8").log().all()                             //header("key","value; actualheadervalue")
;

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++




The body response looks like:

[
  {
    "userId": 123,
    "username": "sysadmin",
    "roles": [
      "ROLE_OPERATOR",
      "ROLE_ADMIN"
    ]
  }
]
I want to assert the roles array contains at least "ROLE_ADMIN". So I wrote this test:

RestAssured.given(...).get(...)
  .then()
    .statusCode(200)
  .and()
    .body("roles", hasItem("ROLE_ADMIN"));
	
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++	
	
	
	@Test
public void givenMovieId_whenMakingGetRequestToMovieEndpoint_thenReturnMovie() {

    Movie testMovie = new Movie(1, "movie1", "summary1");
    when(appService.findMovie(1)).thenReturn(testMovie);

    get(uri + "/movie/" + testMovie.getId()).then()
      .assertThat()
      .statusCode(HttpStatus.OK.value())
      .body("id", equalTo(testMovie.getId()))
      .body("name", equalTo(testMovie.getName()))
      .body("synopsis", notNullValue());
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

We can also extract the whole response to a String, using the extract().asString() API:

String responseString = get(uri + "/movie/" + testMovie.getId()).then()
  .assertThat()
  .statusCode(HttpStatus.OK.value())
  .extract()
  .asString();
assertThat(responseString).isNotEmpty();
Copy
Finally, we can extract a particular field out of the response JSON as well.

Let’s look at a test for a POST API that expects a Movie JSON body and will return the same if inserted successfully:

@Test
public void givenMovie_whenMakingPostRequestToMovieEndpoint_thenCorrect() {
    Map<String, String> request = new HashMap<>();
    request.put("id", "11");
    request.put("name", "movie1");
    request.put("synopsis", "summary1");

    int movieId = given().contentType("application/json")
      .body(request)
      .when()
      .post(uri + "/movie")
      .then()
      .assertThat()
      .statusCode(HttpStatus.CREATED.value())
      .extract()
      .path("id");
    assertThat(movieId).isEqualTo(11);
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++	

3.3. JSON Array
We can also verify the response if it’s a JSON array:

@Test
public void whenCallingMoviesEndpoint_thenReturnAllMovies() {

Set<Movie> movieSet = new HashSet<>();
movieSet.add(new Movie(1, "movie1", "summary1"));
movieSet.add(new Movie(2, "movie2", "summary2"));
when(appService.getAll()).thenReturn(movieSet);

get(uri + "/movies").then()
    .statusCode(HttpStatus.OK.value())
    .assertThat()
    .body("size()", is(2));
}
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

4. Validating Headers and Cookies
We can verify a header or cookie of the response using methods with the same name:

@Test
public void whenCallingWelcomeEndpoint_thenCorrect() {
    get(uri + "/welcome").then()
        .assertThat()
        .header("sessionId", notNullValue())
        .cookie("token", notNullValue());
}
Copy
We can also extract the headers and cookies individually:

Response response = get(uri + "/welcome");

String headerName = response.getHeader("sessionId");
String cookieValue = response.getCookie("token");
assertThat(headerName).isNotBlank();
assertThat(cookieValue).isNotBlank();

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
validate nested array
"token":"123456";
"data":{

"user":[
       {"id":1,"name":"john"},
	   {"id":2,"name":"Hani"}   
]
}
.then
.body("data.user[0].id", equalsTo(1))
.body("data.user[0].name" ,equalsTo("john"))

.body("token", notNullValue());

TestNG
Assert.assertEquals("data.user[0].name","john");

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++


	








 
        
        
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
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Handling WebTable

int totalrows= driver.findElements(By.xpath("//table[@class='tablename']//tbody//tr")).size();
int totalcols= driver.findElements(By.xpath("//table[@class='tablename']//tbody//td")).size();

for(int i=1;i<=totalrows; i++)
{
for(int j=1;j<=totalcols; j++)
{
String Tabledata= driver.findElement(By.xpath(By.xpath("//table[@class='tablename']//tbody//tr["+i+"]/td["+j+"])).getText();

}

System.out.println(Tabledata);

}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Handling Dynamic WebTable

String text = driver.findElement(By.xpath("//div[contains(text(),"pages")]")).getText();


int totalPages= text.substring(text.indexOf("(")+1, text.indexOf("pages")-1);

//Integer.parseInt - Convert String value in to Integer

int totalPages= Integer.parseInt(text.substring(text.indexOf("(")+1, text.indexOf("pages")-1));

//Repeating pages

for(int p=1; p<=totalPages; p++)
{
if(p>1)
{
WebElement activepage = driver.findElement(By.xpth("//ul[@class='pagination']"))//*[text()="+p+"]);

activepage.click();
Thread.sleep(3000);
}

//Reading data from Table

int totalrows= driver.findElements(By.xpath("//table[@class='tablename']//tbody//tr")).size();

for(int i=1;i<=totalrows; i++)
{

driver.findElement(By.xpath(By.xpath("//table[@class='tablename']//tbody//tr["+i+"]/td[3])).getText();


}

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


packages4

1- Base Test
class1
we have created base class in we intialise our webdriver browser/Restassured.

2- POM
class1- Login page, bankslink - login ID and Password.
class2- Txn Seach page
class3 - Initialize the driver.

3- Utility- @Data Provider utility, and extend report utility.

4-Test Cases- Based on requirement we will create test case classes.

5- Resouce folder - Log4j for logging mechanism, config property - values for Login page teller id and passord.

6- Project is maven based so we have added all dependencies in pom.xml.

7- Screenshots folder- for failure test cases.

8- Report folder - extend report generation.

9- TestNG.xml file - for parallel test cases run, and grouping the test cases.


}


