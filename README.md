# Assignment-4-Data-Processing-solution

Download Here: [Assignment 4 Data Processing solution](https://jarviscodinghub.com/assignment/assignment-4-data-processing-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

In this assignment, you will be performing some important data-processing
operations, specifically sorting a large database file. Sorting data is a very
important operation in computing for many reasons. One of those reasons is that it makes the data more accessible to humans once it is printed (imagine trying to use a telephone directory in which the names do not appear in any particular order).

Another reason is that it makes the data more quickly searchable by the computer.

There are many large data files to use for this assignment, but you will
only need the first one until you get on to the advanced parts. They are all
available on blackboard, and are named people1.txt, people2.txt, people3.txt,
people5.txt, people10.txt, people20.txt, people30.txt, people50.txt, and
people100.txt.

Look at the file “people1.txt” with a text editor. You will see that it
contains data about a number of people. Each line contains exactly five items: a
person’s social security number, their first name, their last name, their date of
birth, and state of residence. The five items are separated by spaces, but no item
will ever contain a space. Here is a sample from the middle of thefile:

320990814 Arthur Farmer 19560424 NV
322230050 Eros Crandon 19250819 TX
324640114 Lusitania Lissom 19440104 IN
325400784 Rose Terwilliger 19260122 WI
327640597 Jeffrey Stone 19760801 DE
327950765 Mary Emmett 19290224 CO
328610085 Heironymous Inchworm 19661102 CA
329310410 William McCormick 19550819 WV
329320248 Nicola Birchmore 19230107 IA
330270343 Pauline McTaggart 19290402 MN
331130693 Jim Trombone 19411222 NE
331960453 Abraham Larch 19750901 WY
332040687 Trixie Underwood 19200516 UT

As you may have noticed, the date of birth is provided as a single integer, in the format yyyymmdd; Arthur Farmer was born on the 24th of April 1956. The 1 in the filename people1.txt indicates that it contains exactly one thousand lines.

1. Read the Data
Write a program that creates a list large enough to hold all the data, then reads all the data from the file into that list. Of course, it will have to be a list of structs that you will also need to define. Make your program close the file, then print out the first 10 items of data from the list, so that you can make sure everything was read correctly.

2. Basic Search
Make your program ask the user to enter a name. It should then search through the data in the list (don’t read the file again), finding any entry with a matching name. Correct matches with either first or last name should be accepted. For every matching entry that is found, print out all four data items: the social security number, first and last names, and date of birth of each matching person.
Remember that if you use the == operator to compare strings, the test is case-sensitive.
The user (i.e. you) will have to type the name exactly correctly, with capital letters in the right places.
Important: Good clean design will make this lab much easier. Write a separate function that searches the list, do not put all the work in main.

3. Find the Oldest
Modify your program so that after closing the file, instead of printing the first ten items of data, it searches through all of them to find the oldest person represented. It should print the social security number, first and last names, date of birth, and state of the oldest person found.
Important: As for part two, good clean design will make this lab much easier. Write a separate function that searches the list to find the oldest person, do not put all the work in main.

4. Promote the Oldest
For some unfathomable reason, the management wants the oldest person to occupy the first position in the list. Modify your program so that after finding the oldest person, it swaps his or her data with the data already occupying the first position in the list. Remember that the first position in a list is numbered zero, not one.

5. Now Promote the SecondOldest.
The management has now decided not only that the oldest person must occupy the first position in the list, but also that the second-oldest person must occupy the second position in the list. So, after searching for the oldest and moving their data to the front of the list, now search the remainder of the list (all except the first element), and move the oldest person you find (which must be the second oldest of all) into the second position of the list. Make sure you swap data, so that whoever was originally in the second position is not lost.

6. More of the Same.
The management are going to keep on adding requirements like this, next putting the thirdoldest in the third position, then the fourth, then the fifth. There is no knowing when they will grow out of this petty obsession, so make things easier for yourself. Modify your search function so that it can be told how much of the list to search. That is, give it two int parameters (let’s call them a and b); its job is now to search only the portion of the list between position a and position b, to find the oldest person therein. This makes it very easy to search the remainder of the list to find the second and third oldest.

7. The Ultimate Demand.
Now the management make their final demand. You are to repeat the process of moving the nth-oldest person into the nth position 1000 times. (please remember, 1000 is the number of data records in the whole file).
This will result in the list being completely sorted. Do it, and check that it worked. Make your program print the contents of the list after it has finished. Look at the output to make sure that everyone is printed in order of their age.
Try to implement your own selection sort function – instead of using the Python sort.

8. Sorting the File.
Once you have sorted the contents of the list, it might be a good idea to save the sorted data in a file. Make your program create a new file, and write all the contents of the list into that file in a sensible format. Use a text editor to look at the file and verify that it has the same format as the original file, and all the data is properly sorted.

9. How Fast Is It?
It is important to know how long computer operations are going to take when they have to work on a large amount of data.
Use a function (twice) to time how long it takes the computer to sort the list of 1000 data items. Do not include the time it takes to read the file or the time it takes to write the new file, just the pure sorting time. Note the time that you observe.
Now you know how long it takes to sort a database of 1000 items. How long do you think it would take to sort a database of 2000 names? 3000 names? 10,000 names?
Think about those questions, and work out what you believe the answer is. Then find out what the real answer is. The other files have exactly the same format as people1.txt, but are longer. PeopleN.txt contains N thousand data records. If your program was nicely written, it will be a few seconds’ work to change the list size and make it read a different file.
See how long it takes to sort these larger files, and compare the results to your
predictions. If your predictions weren’t substantially correct, make sure you understand why. You have just demonstrated a very important phenomenon of computing.

10. Friendships (Extra Credit Only – 200 Points)
a. Copy your code to a separate program.
b. You will work with the list of persons.
c. Implement or use a function random_in_range(int a, int b) function to choose a
random integer number between two integers.
d. Add a friends list for your PersonType class.
e. For each person in the person list choose a number of friends (minimum is zero and maximum is Size/200). Assume this number is x. Now you need to generate x
locations of the friends and add them as friends to the list of friends of the current
person.
f. Write or use a function that will sort the list now by the number of friends in a
descending order.
g. For each person, find other people who have common friends with that person and who those common friends are.
h. For each person, find all the people who have that person as a friend.
i. Repeat part e to randomly unfriend people (unfriending is zero to half of the number of friends).
j. Repeat part f after you have run the unfriend part
