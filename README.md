## Facebook Comment Scraper

<!--TABLE of contents-->
<h2> Table of Contents </h2>
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Prerequisite">Prerequisite</a></li>
    <li><a href="#Commands">Commands</a></li>
    <li><a href="#Usage">Usage</a></li>
    <li><a href="#Explanation">Explanation</a></li>
    <li><a href="#Contact">Contact</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>

<!--TABLE of contents //-->

## Prerequisite
1. Python 3
2. Virtualenv
3. Download Web Driver, follow the documentation of drivers [here](https://pypi.org/project/selenium/)
<br>
<hr>
<br>

## Commands

#### Clone the repository
```
git clone https://github.com/sajaldoes/FacebookScraper
```

#### Go to the directory
```
cd FacebookScraper
```

#### Create cirtual environment
```
virtualenv fb_scrap
```

#### Activate virtualenv
```
source fb_scrap/bin/activate
```
#### Install pip libraries
```
pip install -r requirements.txt
```

<br>
<hr>
<br>

## Usage

* Make your CSV file like this example - 

| Id      | link |
| ----------- | ----------- |
| 0     |  https://mbasic.facebook.com/example_post      |
| 1   | https://mbasic.facebook.com/example_post       |

* Save the file on the directory as `posts.csv`
* Provide Email and password of your facebook account while executing the code snippet - 

```python
# Login with Username and Password
username = driver.find_element('xpath','//*[@id="email"]')
my_username = getpass(prompt="Your Facebook email or phone:")
username.send_keys(my_username)

password = driver.find_element('xpath','//*[@id="pass"]')
my_password = getpass(prompt="Your Password:")
password.send_keys(my_password)

password.send_keys(Keys.RETURN)
```
* Execute rest of the code for getting the crawled data.
* Comments will be added `comments.csv` file.

<h3 id="scraperParameters"> Functions and variable Explanation </h3>
<table>
<th>
<tr>
<td> <b>Terminology</b> </td>
<td> <b>Type</b> </td>
<td> <b>Description</b> </td>
</tr>
</th>

<tr>
<td>
comment_texts
</td>
<td>
List
</td>
<td>
A list of strings where all the comments are appended.
</td>
</tr>

<tr>
<td>
link_index
</td>
<td>
List
</td>
<td>
A list of integers where all the post link indexes are appended.
</td>
</tr>

<tr>
<td>
comment_crawl()
</td>
<td>
Function
</td>
<td>
A function find the elements of comments and process them to add at the comment_texts list. It takes i as input which is the index of the link.
</td>
</tr>

<tr>
<td>
replies_crawl()
</td>
<td>
Function
</td>
<td>
A function find the elements of replied button then go through the page, find the comments and process them to add at the comment_texts list. It takes i as input which is the index of the link.code>
</td>
</tr>

<tr>
<td>
replied_btn
</td>
<td>
Object
</td>
<td>
An object find the elements of reply button by xpath
 </code>
</td>
</tr>

<tr>
<td>
comments
</td>
<td>
Object
</td>
<td>
An object find the elements of comment texts by xpath
 </code>
</td>
</tr>

<tr>
<td>
mentions
</td>
<td>
Object
</td>
<td>
An object find the elements of mention on replied comments by xpath
 </code>
</td>
</tr>

<tr>
<td>
more_btn
</td>
<td>
Object
</td>
<td>
An object find the element of more button on the page by xpath
</td>
</tr>

<tr>
<td>
cmnt
</td>
<td>
String
</td>
<td>
A string which is a stripped comment text
 </code>
</td>
</tr>

<tr>
<td>
comments_df
</td>
<td>
Dataframe
</td>
<td>
A dataframe with link index and comment texts
 </code>
</td>
</tr>

<tr>
<td>
posts
</td>
<td>
Dataframe
</td>
<td>
A dataframe read from the `posts.csv` file where the links are stored.
 </code>
</td>
</tr>
</table>

<br>
<hr>
<br>


## Contact

[Shumaiya Akter Shammi](https://github.com/Shammi179)<br>
shumaiya15-12179@diu.edu.bd <br>
[Sajal Das](https://github.com/sajaldoes)<br>
sajal15-12381@diu.edu.bd <br>

## License