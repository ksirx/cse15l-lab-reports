__Name: Xavier Navarro__

__CSE 15L Lab Report 3__

During weeks 4 and 5, I learned about some useful commands that I can use in bash. Some of these prominent commands are ```find```, ```less```, and ```grep```. Lets dive further and explore more ways to implement the ```grep``` command!

__Variation 1__

One variation is the ```$ grep -w <term> <filename>``` which finds the specified word is in the files. Here are some examples of what the use of this command returns.

Example 1:

IMG

In this image the command ```$ grep -w "absolutely" */*``` was used. As you can see, the result is lines from everything inside technical which also have the term "absolutly".

Example 2:

IMG

Similar to the last example, the command ```$ grep -w "weather" */*``` was used. This command looks for all instances of the word "weather" and returns it to the terminal.

I learned about this variation through this website: https://www.geeksforgeeks.org/grep-command-in-unixlinux/.

__Variation 2__

The second variation that I was able to find is the ```$ grep "^term" <filename>``` which finds all files which start with the desired term. Here are two examples of this in action.

Example 1:

IMG

Here, you can see that the command ```$ grep "^About" */*/*``` was used. In the output, you can see that it identifies every line that has "About" at the very frint of the line.

Example 2:

IMG

The command ```$ grep "^what" */*/*``` was used here. Similar to the last image, you can see that it finds the term "what" when its at the front of the line. It is important to note that this example proves that it is case-sensitive.

I learned about this variation through this website: https://www.geeksforgeeks.org/grep-command-in-unixlinux/.

__Variation 3__


__Variation 4__

