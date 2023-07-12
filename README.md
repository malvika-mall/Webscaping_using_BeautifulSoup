# Webscaping_using_BeautifulSoup
This is a mini project for Webscraping Data from Real Website using Python Library for BeautifulSoup. I am here going to extract the list of United States Largest Companies by Revenue using below web link.

Website_URL:"https://en.wikipedia.org/wiki/List_of_largest_companies_in_the_United_States_by_revenue"

# Code Snipets:
<details>
  <summary><strong>Importing Libraries</strong></summary>
  <p>

  ```python
  from bs4 import BeautifulSoup
  import requests

  # Defining URL and parsing using HTML
  url="https://en.wikipedia.org/wiki/List_of_largest_companies_in_the_United_States_by_revenue"
  page=requests.get(url)
  soup= BeautifulSoup(page.text, 'html')
```
<details>
  <summary><strong>Table Extraction and Header Elements</strong></summary>
  <p>

  ```python
  table = soup.find_all('table')[1]
  world_titles = table.find_all('th')
  print(world_titles)

```
<details>
  <summary><strong>Iterating through Column Data and Fetching Individual Row Data</strong></summary>
  <p>

  ```python
  for row in column_data[1:]:
      row_data = row.find_all('td')
      individual_row_data = [data.text.strip() for data in row_data]
    
      length = len(df)
      df.loc[length] = individual_row_data

```
** View Jupyter Notebook for complete code**
