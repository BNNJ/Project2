# scraper

A simple webscraper to gather book data from http://books.toscrape.com

## setup

First clone the repo :
```bash
git clone https://github.com/BNNJ/Project2.git
```
or with gh CLI:
```bash
gh repo clone BNNJ/Project2
```

Then go into the directory and make a virtual environment:
```bash
cd Project2
python3 -m venv .
```

Source the environment script:
| Platform    | Shell             | Command to activate virtual environment |
| ------------|-------------------|---------------------------------------- |
| POSIX       | bash/zsh          | `$ source ./bin/activate`               |
|             | fish              | `$ source ./bin/activate.fish`          |
|             | csh/tcsh          | `$ source ./bin/activate.csh`           |
|             | PowerShell Core   | `$ ./bin/Activate.ps1`                  |
| Windows     | cmd.exe           | `C:\> .\Scripts\activate.bat`           |
|             | PowerShell        | `PS C:\> .\Scripts\Activate.ps1`        |

now install required modules:
```bash
pip install -r requirement.txt
```

## usage

```bash 
./scraper.py [-h] [-d | -q] [--nosave] [file]
```

## arguments

argument       | effect
---------------|-------
file           | the csv file to write to (default 'books.csv')
-h, --help     | show help message and exit
-d, --debug    | enable debug logs
-q, --quiet    | silence the info logs
--nosave       | don't save to csv
-i, --images   | save images

## examples

Save scraped books information to books.csv:
```bash
./scraper books_data.csv
```

Save images but not the text data, in quiet mode
```bash
./scraper --images --nosave -q
```