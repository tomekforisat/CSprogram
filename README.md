# CSprogram
This program attempted to create a receipt from specific input.


import java.util.Scanner;
/** 
* CS149 Bakery PA.
* This program will ask for a variety of inputs 
* and it will give you the output of the final price. 
*
* @author Zack Tomek
* @version 09/07/2018
* Acknowledgements: I received no outside help on this assignment and have 
  * abided by the JMU Honor Code.
*/

public class Bakery
{
/** 
* This method will ask for inputs of name, date, price, item code, and discount 
* and will calculate the final price.
* 
* @param args the main input of the name, date, price, item code, and discount
*/

 
   public static void main(String [] args)
   {
      Scanner keyboard = new Scanner(System.in);             //All of the input 
      System.out.print("What is your first name? ");
      String firstName = keyboard.nextLine();
      System.out.print("What is your last name? ");
      String lastName = keyboard.nextLine();
      System.out.print("What is the item code? ");
      String itemCode = keyboard.nextLine();
      System.out.print("What is the quantity? ");
      int itemNumber = keyboard.nextInt();
      System.out.print("What is the price? ");
      double itemPrice = keyboard.nextDouble();
      System.out.print("What is the discount percent in decimal form? ");
      double itemDiscount = keyboard.nextDouble(); 
       
      double initialCost;                         //Calculating for the reciept 
      initialCost = itemNumber * itemPrice;
      double discountActual;
      discountActual = itemDiscount * initialCost;
      double discountPrice;
      discountPrice = initialCost - discountActual;
      double itemTax;
      itemTax = .053 * discountPrice;
      double taxPrice;
      taxPrice = (initialCost - discountActual) * 0.053; 
      double finalCost;
      finalCost = discountPrice + itemTax;
        
      System.out.println("*****                  *****");  //The actual receipt 
      System.out.println("\\___/ BRENDON'S BAKERY \\___/");
      System.out.println();
      System.out.println(firstName  + " " + lastName);
      System.out.println("Date: 09/07/2018");
      System.out.println();
      System.out.println("Product   Qty   Price");
      System.out.println("-------	  ---	-----");
      System.out.println(itemCode + "     " +  itemNumber + "    " + itemPrice);
      System.out.println();
      System.out.println("Initial Cost:  " + "$" + initialCost);
      System.out.println("Discount at 10.0%: " + discountActual);
      System.out.println("Tax at 5.3%: " + taxPrice);
      System.out.println("Final Cost: " + finalCost);
      System.out.println();

   } } 
