/******************************************************************************
* AUTHORS    : Devlin Hamidjaja & Sebastian Hooshmand
* STUDENT ID : 1047448
* LAB #16    : Party Planner
* CLASS      : CS1A
* SECTION    : MW: 8am
* DUE DATE   : 3/14/18
*******************************************************************************/

#include <iostream>
#include <iomanip>
using namespace std;

/******************************************************************************
 * Party Planner
 *-----------------------------------------------------------------------------
 *	This program will output which snack and beverage will be served to their
 *		friend
 *-----------------------------------------------------------------------------
 * INPUT:
 *    name : Guest's name
 *    age  : Guest's age
 *    choc : If they like chocolate
 *    nuts : If they like nuts
 *
 * OUTPUT:
 * 	  Guest's name, snack and drink
 ******************************************************************************/
int main()
{
	/**************************************************************************
	 * CONSTANTS
	 * ------------------------------------------------------------------------
	 * OUTPUT - USED FOR CLASS HEADING
	 * ------------------------------------------------------------------------
	 * PROGRAMMERS : Programmer's name
	 * CLASS      : Student's Course
	 * SECTION    : Class Days and Times
	 * LAB_NUM    : Lab Number (specific to this lab)
	 * LAB_NAME   : Title of the Lab
	 **************************************************************************/
	const char PROGRAMMERS [] = "Devlin Hamidjaja & Sebastian Hooshmand";
	const char CLASS[]        = "CS1A";
	const char SECTION []     = "MW: 8am-11:50am";
	const int  LAB_NUM        = 16;
	const char LAB_NAME[]     = "Party Planner";
	const int  OUT_WIDTH      = 30;
	const int  MAX_NAME       = 25;
	// variable declarations
	char name[MAX_NAME];
    int  age;
    char choc;
    char nuts;

	// OUTPUT - Class Heading
	cout << left;
	cout << "**************************************************\n";
	cout << "*  PROGRAMMED BY : "  << PROGRAMMERS << endl;
	cout << "*  "      << setw(14) << "CLASS"     << ": " << CLASS    << endl;
	cout << "*  "      << setw(14) << "SECTION"   << ": " << SECTION  << endl;
	cout << "*  LAB #" << setw(9)  << LAB_NUM     << ": " << LAB_NAME << endl;
	cout << "**************************************************\n\n";
	cout << right;

	/**************************************************************************
	 * INPUT - read's in the name and age of the user, and if they like
	 * chocolate and nuts
	 **************************************************************************/
	cout << left;

	cout << setw(OUT_WIDTH) << "What is your friend\'s name?";
	cin.getline(name, MAX_NAME);

	cout << setw(OUT_WIDTH) << "How old is your friend?";
    cin  >> age;

    cin.ignore(1000,'\n');

    cout << setw(OUT_WIDTH) << "Do they like chocolate (Y/N)?";
    cin.get(choc);


    cin.ignore(1000,'\n');


    if(choc == 'Y')
    {
    	cout << setw(OUT_WIDTH) << "Do they like nuts (Y/N)? ";
    	cin.get(nuts);
    	cin.ignore(1000,'\n');
    }

    cout << endl;


    /**************************************************************************
     * PROCESSING - <none>
   	 **************************************************************************/

    /**************************************************************************
    * OUTPUT - User's snack and drink
    ***************************************************************************/
   if(age >= 21)
   {
	  if(choc == 'Y')
      {
		  if(nuts == 'Y')
          {
             cout << "You should serve " << name << " Peanut M & M's and beer.";
          }
          else
          {
         	 cout << "You should serve " << name << " M & M's and beer.";
          }
       }
       else
       {
    	   	 cout << "You should serve " << name << " Skittles and beer.";
       }
   }
   else
   {
	   if(choc == 'Y')
       {
		   if(nuts == 'Y')
		   {
			 cout << "You should serve " << name << " Peanut M & M's and soda.";
           }
           else
           {
        	 cout << "You should serve " << name << " M & M's and soda.";
           }
       }
       else
       {
        	 cout << "You should serve " << name << " Skittles and soda.";
       }
    }
    return 0;
}
