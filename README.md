# Python Learning Notes

**Always check your code thoroughly before asking for help. Ref: request Cross Site error caused by `[]`**

## system
1. use `pyenv` to get around root privileges
2. use `Anaconda` to get around compiling restriction
3. Anaconda missing packages:
 * plotly

## Crontab
### Allow relative Path in crontab:
1. crontab can use cd to change working directory
2. `#!` can be changed to pyenv .shim
3. .py file need to be excutable `chmod +x`
4. Sample crontab command

        . ~/.bashrc
        cd /home/liuyidh/laviex/pyreport/
        ./ALL_report.py`

## Python:
1. use map() to simplify things
2. use list comprehension to flatten a nested list/dict
        
        [b for dic in [dict1, dict2, dict3] for (a,b) in dic.items()]

3. use dict / list comprehension for powerful process:

        info = {k: [x.strip() for x in v] for (k, v) in info.iteritems()}
        
        

        Use a dictionary when you have a set of unique keys that map to values.
        Use a list if you have an ordered collection of items.
        Use a set to store an unordered set of items.

4. filter empty string:

        str_list = filter(None, str_list)
        
5. use functools.partial to freeze/set certain arguments
6. remember to close file to finish writing.
7. syntax brackets error due to sublime autocompletion
8. memory release
    * del + gc.collect()
    * multiprocessing
    * divide into smaller chunks then use shell script to run one by one
9. class Object does not update automatically if you revise the class **after** the object is created.
10. Fucntions: reuse, readability, avoid redundancy
    * KimPeek 2 years ago
    * Functions should be small, sharp tools that do one thing well. This is a guideline, not a hard rule, but you should generally make a new function for each code block. Every loop, try/except block, whenever you indent more than 3 times, and anytime you are doing more than one thing.

## Pandas:
1. use astype(float) to change stype
2. pandas-datareader 0.5.0 not available from conda, use pip instead, no need to downgrade

## lxml:
1. be careful with JS re-written attributes and capitalization.
2. be careful with text with /t/n spaces
3. be careful wih variable explorer

## Web2py:
1. how to uWSGI
2. how to multiple domains
3. use nohup xxxx & to run background or use screen to run ssh tunneled python admin
4. use crontab @reboot to start web2py.py -K app
5. define table
6. use request.args to dynamicly define variables (mailer headers etc.)
7. request.requires_https() includes redirect and session.secure() [link](https://groups.google.com/forum/#!msg/web2py/RHwSWU5sqqA/UlXCmJ3VmCoJ)
