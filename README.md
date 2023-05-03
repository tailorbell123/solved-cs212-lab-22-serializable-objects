Download Link: https://assignmentchef.com/product/solved-cs212-lab-22-serializable-objects
<br>
<strong>Serializable Objects.</strong>

A Serializable object is one that can be written to a file and read from a file. The file contains non-ASCII codes representing the state of the object. If you tried to edit a file containing Java objects you would see garbage, because only Java knows how to read and write the information about the objects themselves.

Any class that implements the interface Serializable (found in java.io.* which must be imnported) may have instantiated objects written to and read from a file.




Create a new Eclipse project for Lab22.




Import the classes ReadDate and SaveDate from Z:Lab22 or from Blackboard, and look at the code.  Run SaveDate first: this will create a file and save a Date object in it. Then run ReasDate and see that object was read from the file, cast as a Date, and printed.




Now copy your Money, Bill, Coin and Quarter classes from Lab 17 to this project. Create classes called ReadMoney and SaveMoney and (to save time) cut ans paste the code from ReadDate and SaveDate into these two classes. You will need to change some of the types and variables so these new classes work on Money.




Be sure class Money imports java.io.*, and change the heading of Money so it reads

Public class Money implements Serializable {

So Money (and its subclasses) will be serializable objects.




Have SaveMoney create a Quarter and write it to a file. Then have ReadMoney retrieve the Quarter from the file.




Now insert a loop in SaveMoney so that several Quarters (or better yet, several types of Coins) are written to the file, then in ReadMoney read all the coins from the file.