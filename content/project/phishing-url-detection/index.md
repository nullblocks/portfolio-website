---

title: "Phishing URL Detection"
subtitle: ""
summary: "Project aimed to protect users from phishing websites by identifying and alerting them to potential threats, as well as blocking ads through the use of a tool such as pi-hole"
authors: []
tags: ["ml" , "phishing attack" , "flask" ]
categories: []
date: 2023-07-11T17:57:53+05:30
lastmod: 2023-07-11T17:57:53+05:30
featured: false
draft: false

image:
  caption: ""
  focal_point: ""
  preview_only: false

url_code: "https://github.com/nullblocks/phishing-url-detection"
url_pdf: "/project/phishing-url-detection/Report.pdf"
url_slides : "https://github.com/nullblocks/phishing-url-detection/blob/master/Report/SEM6%20P1.pdf"

projects: []
---
### what is phishing ? 
When it comes to cyberattacks, phishing remains as one of the ever- popular techniques  use for malicious intents. Phishing is a type of attack which combines technical tactic and social engineering in an attempt to obtain personal or otherwise sensitive information such as login credentials, credit card details, or company secrets from the victim
![Phishing-gif](/project/phishing-url-detection/phishing.gif)


### Architecture
![Architecture](https://user-images.githubusercontent.com/110848103/252778421-954e9986-952f-4207-aae1-efe728b0ae79.png)


* We will train the ML model with Phishing and non phishing urls having 30 different feature set . 

* Chrome extension will observe the URL / website that we visit . 

* `features.py` will extract all 30 features from URL and ML mode will classify wheather it is phising website or not . 

* If it classify as phishing website then it will warn the user about it .

![extension](/project/phishing-url-detection/Extension.png)
<pre>               fig : Extension Warning user of phishing website </pre>

### One Problem we observe 

During the reaseach of this project we observe that now a days phishing URL are spread through the ads campaign and many people fall for it . 

![phishing-add](/project/phishing-url-detection/Phishing-add.png)

Top search results are all phishing website which have alterated version of OBS software which have malware , Cyber Security reasearcher found this .Now it have solved  when it came into limelight . 

#### So we impement an ad-blocker using `pi-hole` .

* Pi-hole is great for an organization because it block at DNS level and no need it install on every device . 

* It have dashboard , stastics and we can block different site at DNS level. 
{{% callout note %}}
Watch pi-hole demo by clicking on Image 👇👇👇
{{% /callout  %}}

[![Watch the video](https://img.wonderhowto.com/img/90/94/63691092220921/0/lock-down-your-dns-with-pi-hole-avoid-trackers-phishing-sites-more.1280x600.jpg)](https://youtu.be/gfnYoKWvoSk)

### Output 

![HomePage](https://user-images.githubusercontent.com/110848103/240217193-9737bbd1-1828-48e0-96a1-70b640b183eb.png)

<pre>                        Webapp to check phishing URL</pre>

![Blocked-Ads](/project/phishing-url-detection/blocked-dns.png)
<pre>               Fig : Blocked URL / domain going to Ads Server .</pre>

