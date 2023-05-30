Jacob Reiser

For this project, I implemented the designated functions in file.c and directory.c,
df, stat, create, cat, cp, rm, ln, ls, mkdir, rmdir, and cd. I tested the funcitonality
by running the fs_sim using the test inputs and saving the output to a file and running the 
fs_sim_reference with the same inputs and saving the output to a reference file. Then I 
checked the difference of the two files and tweaked the differences until the output of 
both operations matched. 

I'm not sure how in-depth to go with the explanation. But in most instances for the directory 
functions was a combination of using the inode for reading/writing from the directory block and 
loops to ensure the data was copied/deleted properly. Loops were the main design in almost all of
the file functions, mostly looping thorugh the blocks and content of the blocks to either read,
write, copy, or remove from the Inodes. In the places where loops were not used, such as the hard
link, it was a process of using the inode and the current directory information with the dentry
in the correct sequence of reading and writing in order to generate a new link.
