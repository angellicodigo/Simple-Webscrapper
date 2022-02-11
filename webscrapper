import requests
from bs4 import BeautifulSoup

urls = ["https://proofwiki.org/wiki/Definition:Absolute_Geometry", "https://proofwiki.org/wiki/Definition:Abstract_Algebra", "https://proofwiki.org/wiki/Definition:Abstract_Geometry"]

list_ = []

for url in urls:
    dict_ = {}
    html = requests.get(url)

    soup = BeautifulSoup(html.content, "html.parser")

    content = soup.find_all('p')

    heading = soup.find_all('h1')

    branch = heading[0].text[11:]

    definition = content[0].text

    dict_['Branch'] = branch
    dict_['Definition'] = definition

    list_.append(dict_)
    
print(list_)
