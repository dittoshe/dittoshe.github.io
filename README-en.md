# Hydrogen
Lightweight and clean

Follow her footsteps and start your blog journey.


语言：English | [Chinese](README.md)

![hydrogen](/theme/logo-h.svg)

All the handsome guy and beautiful girls gave me stars.Aren't you?:kissing_heart::laughing:~~

# #Quick Start

![hydrogen](/theme/a-h.png)

## #Prepare for the blog

Open `config.yml`in the theme root directory

Modify the following options as required:

`title` : Change your blog name

`description` : Change your blog description

`keywords` : blog keywords (SEO related)

`baseurl` : The directory folder where the blog is located should start with `/`. If it is the root directory, please leave it blank. (It is recommended that the blog be placed in the root directory,Don't make a mistake! Resource files such as style sheets cannot be loaded)

`url` : Your domain name, such as `demo.cn`, does not need to add `http/https://`

`bulidtime` :  the time stamp at the time of blog establishment, which will automatically calculate the time of blog establishment and display in the footer. [Date-to-Time stamp](https://tool.lu/timestamp/)

`paginate` : The maximum number of articles displayed on the home page, which exceeds the set number of articles, is automatically placed on the next page.

`background` : Topic Picture Path on Blog Home Page

`theme_color` : Blog top column color, fill in the color code ** but don't enter # **

`MathJax` : Whether to open MathJax (Boolean value)

`author` : author's name

> Developer options
>> `PJAX` : PJAX Refreshless Loading (Boolean Value)

## # Setting up Domain Name

Modify the CNAME file in the root directory for your domain name

#### The basic settings for the theme have been completed.~

---

## #Friends Links

Open the `friends.yml`file in the `data` directory and add new code according to the template in the file.


---

## #Article Stickie

Add stickie: true to Front Matter

Such as:

```
 ---
 layout: post
 title: Hi
 stickie: true
 ---
```

## #Comment

#### #The premise

> You must make sure that you have read [Valine](https://valine.js.org/quickstart.html)

Configuration file:

`_data/social.yml` :  Fill in app ID and key and comment information

`_includes/comments.html` : comment settings

After making sure the configuration is correct, change the value of "enable" in `data/social.YML` from `false` to `true`

Valine's compatibility may conflict with the Pjax function! If comments are enabled, it is recommended to disable the Pjax function




