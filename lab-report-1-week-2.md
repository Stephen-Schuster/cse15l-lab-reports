# Week 1 CSE 15L Instructions

## Step 1: Install VSCode

First install VSCode from [here](https://code.visualstudio.com/). Click download and follow installation instrucions from there. Once it is set up, open VSCode, which should look like this: 

![Image](vscodeStartup.png)

## Step 2: Remotely Connecting

Next open the command line. On windows, you do this by clicking the start icon or "Type here to search" and then typing "Command Prompt" and double clicking the Command Prompt Application. Then, type the command `ssh cs15lwi22ajb@ieng6.ucsd.edu`. You may need to change the address if you are connecting to a different server than me. If you are another student, the `ajb` will change to something else. Then type in your ucsd password. Note that you won't be able to see what you type the screen will not change at all when you do this. After you're done, it should look like this:

![Image](remoteConnectScreenshot.png)

## Step 3: Try using commands remotely!

Next, make sure your remote connection is working properly by testing out standard commands on the remote machine, maybe some `ls`s and `cd`s and `echo`s. This is what I did:

![Image](tryingCommandsScreenshot.png)

## Step 4: Moving files between local and remote machines with scp

It is important to be able to move files from a local location to a remote machine, which is where the `scp` command comes in. `WhereAmI.java` is a script that prints information about the file path and system that the file is being run on, so we'll use it to test `scp`. The syntax for the command is `scp` then the name of the file to be moved then the address followed immediately by `:~/`. It should look like this:

![Image](scpScreenshot1.png)

![Image](scpScreenshot2.png)

## Step 5: SSH keys

Now, typing in your password every time you want to connect to a remote machine or move a file to a remote machine might be a pain, especially if you have to do it often, so we can avoid that with SSH keys. Follow the following steps to set them up:

![Image](sshKeysScreenshot1.png)

![Image](sshKeysScreenshot2.png)

![Image](sshKeysScreenshot3.png)

## Step 6: Remote Running Optimization

`ssh`ing into the remote machine, running a single command then logging out might be too much of a hassle for one or two commands. So, you can add your command you want to run by adding it on to your `ssh` command and it will run it on the remote machine. 

![Image](remoteRunningOptimizationScreenshot.png)

You can run more than one command in one line by separating them with semicolons. Here is an instance of me doing that. First I `ls` all the files in the remote machines current directory, then I print what is currently in the `newFile.txt` file, then I add a new line to that file and print its contents again, all in 1 line

![Image](remoteRunningScreenshot2.png)

Let's say I copied `WhereAmI.java` to the remote machine, compiled and ran it remotely with `ssh cs15lwi22ajb@ieng6.ucsd.edu "javac WhereAmI.java;java WhereAmI"` and made edits to the file *locally*. How many keystrokes will it take to copy those edits to `WhereAmI.java` on the server and run it with those changes? You only need 7 keystrokes:
1) Click on the terminal to bring it back into focus
2) Hit up arrow
3) Use up arrow again to get back to the `scp WhereAmI.java cs15lwi22ajb@ieng6.ucsd.edu:~/` command
4) Hit enter to run it
5) Hit up arrow
6) Use up arrow again to get back to the `ssh cs15lwi22ajb@ieng6.ucsd.edu "javac WhereAmI.java;java WhereAmI"` command
7) Hit enter to run it

And that's it. Just 7 keystrokes to copy, compile and run local changes on a remote machine.

![Image](remoteRunningScreenshot3.png)

For reference, the highlighted text in the following screenshot is the local change I made to `WhereAmI.java`

![Image](image.png)
