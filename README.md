# FacebookScraper

## Facebook Comment Scraper from Bangla News

<!--TABLE of contents-->
<h2> Table of Contents </h2>
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Prerequisite">Prerequisite</a></li>
    <li><a href="#Commands">Commands</a></li>
    <li><a href="#Usage">Usage</a></li>
    <li><a href="#tech">Tech</a></li>
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



## Team Dynamic DUO
### Sajal Das
#### sajal15-12381@diu.edu.bd


### Shumaiya Akter Shammi
#### shumaiya15-12179@diu.edu.bd
#### Cell- 01843441269