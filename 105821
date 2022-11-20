import mechanicalsoup
from bs4 import BeautifulSoup as bs
from urllib.parse import unquote
from termcolor import colored

browser = mechanicalsoup.Browser()

url = input ("inupt your url ")

login_page = browser.get(url)
login_html = login_page.soup
script = "<script>alert(1)</script>"
form = login_html.select("form")[0]
form.select("input")[0]["value"] = "hjh>"+ script
form.select("input")[1]["value"] = "ThunderDude"
profiles_page = browser.submit(form, login_page.url)

scan2 = profiles_page.url

decode = unquote(colored(scan2,'red'))

if script in decode: 
    print(" congratulations you find XSS " + decode ) 
    #print(colored("[*] Form details:",'red'))
else :
    print("try again")
