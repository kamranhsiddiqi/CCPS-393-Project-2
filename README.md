# CCPS-393-Project-2

Write a C program called "pop" which simulates the operation of a soft drink vending machine. Your program should meet the following requirements.  The user running the program will simulate both service and customer actions. <br />
<br />
Service/Maintenance Requirements
- set the selling price (range 30ï¿½ to $1.05) from a command line argument (cents only)
- provide a specific message (as in sample below) for the following error cases and return to the operating system: 
command line argument is missing
- prices out of range
- price not a multiple of 5
- with a valid selling price, put machine in-service for continual sales (See Customer Requirements)
- as a maintenance action (hidden from menu), allow service person to shutdown (exit) the program altogether at the coin prompt by pressing E or e; refund any pending amount <br />
Customer Requirements
<br />
- First assume that there is only one flavour of pop, and that the machine won't run out of pop (no need to track inventory or total sales)
- display a welcome message stating the pop price, and what coins and commands are accepted
- prompt the user to insert coins (via keyboard entry)
- accept a nickel [N or n], dime [D or d] or quarter [Q or q]; reject all other input except maintenance actions; continually re-prompt if input is invalid
- after each coin, display how much the user has inserted in total and how much more the user needs to insert
- dispense product on collecting sufficient money (only one flavour)
- provide change for overpayment using only dimes and nickels (assume machine won't run out)
- allow user to abort the transaction by pressing coin return (R or r). Refund using only dimes and nickels using the fewest number of coins. 
- continually prompt for additional sales -- do not exit the program
- control flow of your program must match example sequence
 
Example sequence (not exhaustive testing):
$ pop <br />
Please specify selling price as command line argument. <br />
Usage: pop [price] <br />
$ pop 225 <br />
Price must be from 30 to 105 cents inclusive <br />
$ pop 86 <br />
Price must be a multiple of 5. <br />
$ pop 50 <br />
Welcome to my C Pop Machine! <br />
Pop is 50 cents. Please insert any combination of nickels [N or n], dimes [D or d] or quarters [Q or Q]. You can also press R or r for coin return. <br />
Enter coin (NDQR): n <br />
  Nickel detected. <br />
    You have inserted a total of 5 cents. <br />
    Please insert 45 more cents. <br />
Enter coin (NDQR): N <br />
  Nickel detected. <br />
    You have inserted a total of 10 cents. <br />
    Please insert 40 more cents. <br />
Enter coin (NDQR): d <br />
  Dime detected. <br />
    You have inserted a total of 20 cents. <br />
    Please insert 30 more cents. <br />
Enter coin (NDQR): q <br />
  Quarter detected <br />
    You have inserted a total of 45 cents. <br />
    Please insert 5 more cents. <br />
Enter coin (NDQR): j <br />
  Unknown coin rejected. <br />
    You have inserted a total of 45 cents. <br />
    Please insert 5 more cents. <br />
Enter coin (NDQR): Q <br />
  Quarter detected. <br />
    You have inserted a total of 70 cents. <br />
    Pop is dispensed. Thank you for you business! Please come again. <br />
    Change given: 20 cents as 2 dime(s) and 0 nickel(s). <br />
Enter coin (NDQR): q <br />
  Quarter detected. <br />
    You have inserted a total of 25 cents. <br />
    Please insert 25 more cents. <br />
Enter coin (NDQR): R <br />
    Change given: 25 cents as 2 dime(s) and 1 nickel(s). <br />
Enter coin (NDQR): q <br />
  Quarter detected. <br />
    You have inserted a total of 25 cents. <br />
    Please insert 25 more cents. <br />
Enter coin (NDQR): E <br />
    Change given: 25 cents as 2 dime(s) and 1 nickel(s). <br />
Shutting down. Goodbye. <br />
$
