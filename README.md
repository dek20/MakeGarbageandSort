# MakeGarbageandSort

why i did this: I have a large video collection, im interested in someday building a way to organize and search all of these videos in a sophisticated manner with more functionality than standard windows explorer. so i need to understand the basics of manipulating files with code

this code:

makes 500 files randomly named with 4 chars, alphabetic or numeric

makes a subfolder for all chars

deletes all files that contain a '5'

then sorts all the remaining files into the subfolder that matches their first character.


challeneges:

os.walk was a little confusing when iterating through the targeted directory, it took me a bit to understand that it returns a list and how to navigate that, especially for the function that deletes all files with a '5' in the name.

using the open() function i made a lot of mistakes, such as not closing the files after making them. the first few times i was iadvertantly relying on garbage collection to close the files i wasnt using. which left me with a lot of things i couldnt delete until i could figure out what was going on.

firguring out how to handle the errors that potentially would come up with Shutil.move, since my file creation function doesnt have a way to make sure every file name is unique, occasionally i would files with duplicate names. I solved this problem by excepting the Shutil problem with pass, as it when the error was thrown it still seemed to sort all of the file correctly.


