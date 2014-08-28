# Python Learning Notes

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
        
## Pandas:
1. use astype(float) to change stype
2. 

## Web2py:
1. how to uWSGI
2. how to multiple domains
