 Day 1 Commands I learned
   Ctrl + C To cancel when stuck in a command
   ls - list files in current folder
   cd - move to another folder
   cat - show whats inside the file
   find - searching for all the files or for specific ones
   ./ meaning that 'the file is in this folder', its useful for filenames with special characters
   filenames with spaces need quotes like "hello im soroush"
   find . -size 1033c - find the file of an exact size (c is bytes)
   find with -user finds files owned by someone (used to find a password file on the whole system)
   man and --help show how a command works (still kind of confusing, need practice)
   Each level: find a password, use it to log in as the next user, find the next password

 Day 2 Commands I learned
   grep '<the text in the txt file i want to search for>' filename.txt, grep finds text in a txt file
   sort example.txt sorts the txt file 
   sort example.txt | uniq -u, step by step:
   first of all the pipe: | gets the output of the sorted txt and forwards it directly to the other command.
   second of all : uniq merges all of the same text into one , and then -u just takes the text that has been appeared only once and gives it to you.
   also there is uniq -c which puts a count of how many times the line of text has been repeated
   *uniq compares lines that are next to each other, sort sorts the txts lines to be next to each other. Thats why they are used together combined with pipe
   base64 encodes text into a scrambled string, base64 -d decodes it back, also the == at the end is a sign something is base64
   base64 isnt a secret code, it is decodable by anyone
   echo "something" spits out text so for example to pipe into another command
   tr "abc" "efg" turns the letters you give it to the letters you want them to be. tr cant be used on a file directly so i used echo with a pipe to give it text
   gunzip -c file decompresses and prints to screen, useful when the file doesn't have a .gz name so normal gunzip refuses
   tar makes tar balls, tar -x is used to extract them , and at the end you need to put -f so you can write the file name, so like this: tar -xf filename
   bzip2 basically the same thing as gzip, i used bzip2 -d to decompress the file
   file filename basically says what file type is the file
   also forgot to say before that i learned about xxd, it creates hexadecimal dump or reverses it, used it to reverse a file, had to put it in a new file using >
   so i executed: xxd -r data.txt > raw ( -r means reverse, > made a new file named raw and copied everything xxd reversed) xxd wouldnt put its text into the          already made file, so i made a new one, while learning how to make it.
   also strings pulls out printable string from files/data, i used it to find the password for a txt file which had it besides a line of string with === all over it
   (used grep "=" to find the === after the pipe | to find the exact line the password was in)
   For deeply compressed files: run file to see what type it is → decompress with the matching tool → run file again on the result → repeat until file says it's -     - ASCII text → then cat it
    > sends a command's output into a file instead of the screen. command > filename creates (or overwrites) that file with the output
   Don't guess the file type by renaming, run file first, it tells you exactly what it is, then use the matching command. Saves a lot of flailing
   To know if a command changes a file: general rule for compression tools is default=replace, -c=screen only, -k=keep original. When unsure: read --help, or ls       before and after to see what changed, or cp the file first to stay safe
 Day 3 Commands I learned
   Used -i command in SSH to log in, like this: ssh -i keyfile, ssh -i keyfile user@server -p port
   While using it, I encountered a problem my local txt file which had the key was not the correct format. All I had to do was add a newline after the ssh key.
   The newline problem got me stuck for several minutes, felt good finding the answer to my problem!
   Used cat /etc/bandit_pass/bandit14 to read a password file, at first I thought it was a folder, after many errors I used cat because it was a file.
   used netcat + localhost + port to connect to a port inside the localhost
   IP=building/port=apartment
   localhost = 127.0.0.1 = this same computer
   
   
  
