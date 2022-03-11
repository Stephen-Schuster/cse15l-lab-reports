# [Repository Link](https://github.com/Stephen-Schuster/markdown-parse)

# Finding test cases with different results

First, I modified the bash script to print the name of the file before printing the output

![0](lr5img0.png)

Then, I ran the bash script, redirecting the output to a file called `output.txt` for both my group's implementation and the provided implementation.

![1](lr5img1.png)

Finally, I ran diff on the 2 output files. I looked at the line numbers being compared and went into the output files to see which tests gave different results

![2](lr5img2.png)
![3](lr5img3.png)
![4](lr5img4.png)

# Test difference 1: 194

The difference on line 212 was for test file `194.md` which has these contents:

![5](lr5img5.png)

[foo](/bar* "ti*tle")
