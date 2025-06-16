"# Arraychallenge" 
EXERCISE 1-Explanation

    public class ArrayChallenge

        -This defines a class named ArrayChallenge.

        -In Java, all code must be inside a class.

    public static void main(String[] args)

        -This is the entry point of any Java application.

       -When the program runs, execution starts here.

    String[] orderIds = {...}

        -Declares an array of strings called orderIds.

        The array holds a list of order identifiers like "B123", "C234", etc.

    for (String item : orderIds)

        -This is a for-each loop that goes through each element in the orderIds array.

        -On each loop, item holds one string from the array.

    if (item.startsWith("B"))

        -This checks if the current string (item) starts with the letter "B".

        -The startsWith() method returns true if the string begins with the specified prefix.

    System.out.println(item);

        -If the condition is true, this line prints the string to the console.




        EXERCISE 2- Explanation

Random random = new Random();

    -Creates a new instance of Java’s built-in Random class to generate random numbers.

String[] orderIDs = new String[5];

    -Declares an array to hold five OrderIDs.

for (int i = 0; i < orderIDs.length; i++)

    -A standard for loop that will run five times, once for each index in the array.

char prefix = (char)(random.nextInt(5) + 'A');

    -random.nextInt(5) generates a number from 0 to 4.

    -Adding 'A' (which is 65 in ASCII) gives values between 65 and 69, corresponding to characters 'A' to 'E'.

    -(char) casts the resulting int to a character.

int number = random.nextInt(999) + 1;

    -Generates a number between 1 and 999.

    -random.nextInt(999) gives 0 to 998 → +1 shifts it to 1–999.

String suffix = String.format("%03d", number);

    -Formats the number as a three-digit string, adding leading zeros if necessary.

    -For example, 7 becomes "007", 42 becomes "042".

orderIDs[i] = prefix + suffix;

    -Combines the letter and number into a full OrderID string (e.g., B073, E999, etc.).

for (String orderID : orderIDs)

    -A for-each loop that goes through each element in the array.

System.out.println(orderID);

    -Prints each generated OrderID to the console.



    
EXERCISE 3 - Explanation

    Arrays.sort(pallets)
    -Sorts the array alphabetically (lexicographically).

    Collections.reverse(...)
    -Reverses the order of the sorted list.

    Arrays.asList(...)
    -Converts the array into a list so that it can be reversed using Collections.reverse.



    Explanation 4

    Arrays.fill(pallets, 0, 2, null)
    Replaces the elements at index 0 and 1 with null.

    pallets[0].toLowerCase() is only called when the value is not null to avoid a NullPointerException.

    pallets.length is the size of the array (still 4, even after clearing 2 elements).

