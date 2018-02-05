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

## Pandas:
1. use astype(float) to change stype
2. 

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
7. 
