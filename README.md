# Drill-2
Assignment on Drill
# Drills Part 2

## Pipes

1. Download the contents of "Harry Potter and the Goblet of fire" using the command line from https://raw.githubusercontent.com/bobdeng/owlreader/master/ERead/assets/books/Harry%20Potter%20and%20the%20Goblet%20of%20Fire.txt

ANS: CLI---> wget 'https://raw.githubusercontent.com/bobdeng/owlreader/master/ERead/assets/books/Harry%20Potter%20and%20the%20Goblet%20of%20Fire.txt'

2. Print the first three lines in the book

Ans: head -n 3 'Harry Potter and the Goblet of Fire.txt'



3. Print the last 10 lines in the book
solution : tail -n 10 'Harry Potter and the Goblet of Fire.txt'


4. How many times do the following words occur in the book?

    * Harry 
    * Ron   
    * Hermione 
    * Dumbledore 
    
Solution: $grep -o -i Pattern 'Harry Potter and the Goblet of Fire.txt' | wc -l

5. Print lines from 100 through 200 in the book

Solution: head -n 200 'Harry Potter and the Goblet of Fire.txt'|tail -100

6. How many unique words are present in the book?
Solution: tr ' ' '\n' <'Harry Potter and the Goblet of Fire.txt' | sort |uniq -c | wc -l



___________

## Processes, ports

1. List your browser's process ids (pid) and parent process ids(ppid)
Solution: ps -o pid  &&   ps -o ppid

2. Stop the browser application from the command line

3. List the top 3 processes by CPU usage.

Solution: CLI-->  ps --sort=-pcpu | head -n 4

4. List the top 3 processes by memory usage.
Solution:  top -b -o +%MEM | head -10

5. Start a Python HTTP server on port 8000
Solution: python -m http.server 8000

6. Open another tab. Stop the process you started in previous step


7. Start a Python HTTP server on port 90
Solution: python -m http.server 90

8. Display all active connections and the corresponding TCP / UDP ports.
Solution: netstat -a | more


9. Find the pid of the process that is listening on port 5432
 Solution: sudo netstat -ltnp | grep -w ':5432'

____________

## Managing software

Use `apt` (Ubuntu) or `homebrew` (Mac) to:


1. Install `git`, `vim` and `nginx`

Solution: sudo apt install git

          sudo apt install vim

          sudo apt install nginx

2. Uninstall `nginx`

Solution: sudo apt-get --purge remove nginx
_____________

## Misc

1. What's your local ip address?

Solution: curl ifconfig.me


2. Find the ip address of `google.com`

Solution: nslookup www.google.com

3. Where is the `python` command located? What about `python3`?

Solution: env | grep PYTHONPATH

Solution: which python3
