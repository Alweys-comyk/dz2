

from bs4 import BeautifulSoup
import requests



url = "https://books.toscrape.com"
response = requests.get(url)

soup = BeautifulSoup(response.text, "html.parser")

quotes = soup.find_all(class_ = "star-rating Five")



top_books = []


for author in soup.find_all( class_ = "star-rating Five"):
    top_books.append(author.text)

print(top_books)

with open("authors.txt", "w", encoding="utf-8") as file:
    for top_books in top_books:
        file.write(top_books + "\n")
