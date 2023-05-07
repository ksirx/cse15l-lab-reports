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

The third command that I found to be interesting is the ```$ grep "term$" <filename>``` command. The ```$``` in the command means the end of the string and as expected, the use of this is to find wherever it ends with the term. Here are some examples.

Example 1:

IMG

In the first example, ```$ grep "never$" */*/*``` was used and I was trying to find some places that end in "never". You can see that it outputs the expected lines.

Example 2:

IMG

My intention with the command ```$ grep "50$" */*``` was to find some places that end in the number "50". In the output, it ended up finding all places that end in "50" like "250". This shows that this command ignores any spaces and just looks at the last two characters to search for matching lines.

I learned about this variation through this website: https://www.geeksforgeeks.org/grep-command-in-unixlinux/.

__Variation 4__

The final variation that I found was ```$ grep -v "term" <filename>``` which finds and returns everything EXCLUDING the term you have specified. Here's how it works in practice.

Example 1:

IMG

In this first image, you can see the command ```$ grep -v "a" */*``` being used. This command tries to find all lines with exclude the letter "a". In this example, you can see lots of blank lines, which shows that even if it is just a blank line, it will be included in what is returned.

Example 2:

IMG

The second command was ```$ grep -v "E" */*``` and was trying to find all lines where there wasn't any "E". This example shows that it is case-sensitive meaning if you want to filter multiple things, you might need to layer multiple arguements or commands together.

Here is the resource I used to find this command: https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/

__Conclusion__

These were the some of the standout command alterations that I found to be the most interesting. Still, this is only a small portion of what is available for this one command type. Doing more research on this one command opened my eye to how much more there is to learn about bash commands.
