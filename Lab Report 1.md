__Name: Xavier Navarro__

__CSE 15L Lab 1 Report__

A new skill that I learned during Wednesday's lab was how to remotely log into an ieng6 account. This skill opens the door many practical applications and will be a skill that is important to carry into the workforce. This comes in handy especially when you need to run commands or sift through files on your account. At UCSD, we use [ACCOUNTNAME]@ieng6.ucsd.edu.

Here are some important steps you should follow in order to log into an ieng6 account.

__1) Make sure you are able to access ieng6 account.__

This step is key because without your account, you wouldn't have anything to access remotely. There should be an option where you are able sign in to an account using your PID and username (the line of text before the @ucsd.edu) to find your account that you will be using to connect remotely. In this process, you may have to create a passowrd if you haven't already done so. Your username should look like, cs15lsp23[2 unique letters]@ieng6.ucsd.edu.

This is where you find your account and where you would constinue with changing passwords.

![Image](Screenshot (139).png)

__2) Download VSCode__

In order to download VSCode, you need to go to this link, [https://code.visualstudio.com/download](https://code.visualstudio.com/download), and select the apporpriate options that apply to whatever device you are using. Just follow the steps that are on screen and you should be good to go for the next step. If using the CSE lab computers, VSCode may already be installed. This is the program we will be using to in order to access the terminal.

Here is a picture of what you should see if you corectly downloaded VSCode.

![Image](Screenshot (138).png)

__3) Download Git__

Git is a progeam that allows us as the user to have access to shell commands. Here is the website that I used to download Git as I am currently using a Windows device, [https://gitforwindows.org/](https://gitforwindows.org/). The importance of downloading this is it will allow us to access our account remotely. With just VSCode alone, we cannot access the remote server.

This is the website you can use to download Git for Windows.

![Image](Screenshot (140).png)

__4) Connecting Remotely__

To connect remotely, you first need to open up VSCode. In VSCode, you should be able to access the terminal where you want to input the command, ```$ ssh [USERNAME]@ieng6.ucsd.edu```. From here, you should see a pop up asking whether you would like to connect. Enter, ```$ yes ```, to continue.

You will then be prompted to enter a password which which you will enter the password you created for step 1. Note: When entering the password, nothing will appear on the terminal line which is working as an intended security feature. Just enter the password and press enter.

This is what the prompt will look like.

![Image](Screenshot (137).png)

After entering the password, a large chunk of text should pop up on the terminal and you have now successfully connected to the server!

![Image](Screenshot (135).png)

__5) Testing commands__

After connecting to the server, you will now have be able to access commands. In order to utilize these commands, you just need to type into the terminal. Here are some examples of commands that you may find useful.

```$ ls -lat```

This command displays the files in order using the "latest" categpory. In this image, you can see it start from April 9th, and as you go lower, the date goes back to April 5th.

![Image](Screenshot (144).png)

```$ ls -a```

This commmand displays all the files. You can see all the same files from last command, but not in any particular order. All files are listed in a consise manner.

![Image](Screenshot (143).png)

This was a recap of you can connect to a remote server using ssh and git. Thank you for reading and I hope these steps were helpful with getting started with remote connection to your very own ieng6 account!
