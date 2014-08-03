Tasks:
Change into the temporary directory
Using one command, create a directory structure "my/private/files" 
Using one command, create a directory structure "my/public/files"
Create an empty file 't-vars.env' in my/private/files
Using command-line only add the line "List of env vars that begin with T" to the file, make sure it ends with a newline
List all env variables that begin with "T" (hint: you'll need a regex that includes the marker of the start of the line) and append them to the end of the file
export a new variable TESTING_MAKERS=working in such a way that it is still available when you open a new shell
open a new terminal window, check that a new variable is available
output the count of the variables that begin with T to a new file my/public/files/t-vars.count, e.g. "Overall count: 5" (hint: you'll need to use 'command substitution' in bash)
change the permissions of the my/private/files/t-vars.env to make sure that only the owner can read and write the file
change the permissions of the my/private/files directory to make sure that only the owner can change into it
give read and write permissions to all users on my/public/files/t-vars.count
create another file my/public/files/text-files-count.txt and output the number of text files in your home directory (recursively)  into that file
list all env variables sorted alphabetically and show the top 3 lines