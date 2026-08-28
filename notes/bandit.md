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
