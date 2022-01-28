# Code Change 1

![Image](codeChangeScreenshot.png)

https://github.com/Stephen-Schuster/markdown-parse/blob/main/Image.md

![Image](failure.png)

The bug was that the code made no attempt to distinguish links from images because it did not look for exclamation marks at all. This had the effect(the symptom) of listing image names as if they were links. So all we had to do to fix this was simply check to see if there was an exclamation mark before the open square bracket and only add the link if there was no such exclamation mark

https://github.com/Stephen-Schuster/markdown-parse/blob/main/CharacterAfter.md
https://github.com/Stephen-Schuster/markdown-parse/blob/main/InBetween.md
https://github.com/Stephen-Schuster/markdown-parse/blob/main/InfiniteLoop.md
