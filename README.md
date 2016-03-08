##Linkedin Bio Scraper
Parsing linkedin bios by people's names.
Made for the Founders&Devs meetups.

Usage:<br>
1. Install [Python 2](https://www.python.org/) and [pip](https://pypi.python.org/pypi/pip)<br>
2. Create virtual environment (optional, but recommended):<br>
```
$ pip install virtualenv
$ virtualenv <your-dir-name>
$ cd <your-dir-name>
$ source bin/activate
```
to deactivate virtual environment: `$ deactivate`
<br>
3. Clone the repo<br>
```
$ git clone https://github.com/smblance/parse_linkedin_bio.git
$ cd parse_linkedin_bio
```
<br>
4. Install Scrapy and openpyxl: `$ pip install -r requirements.txt`<br>
5. Add the names (first and last names separated by space) into the first row of names.xlsx<br>
6. Run the spider: `$ scrapy crawl parse_linkedin`

The bios will be added to the second row of names.xlsx.<br>
If there are multiple people with the same name, only first person will be parsed.

If you get 999 HTTP response code, try changing USER-AGENT in parse_linkedin/settings.py to the [user agent of your browser](http://whatsmyuseragent.com/).

