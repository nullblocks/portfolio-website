---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Ransomeware Detection"
subtitle: "❗❗❗ Research of Major Project ❗❗❗"
summary: "Detecting ran![Alt text](image.png)someware and their families by doing dynamic analyisis & observing paranoia activity . "
authors: []
tags: [ML , python ,Ransomware , malware , virtualizaion , sandbox .]
categories: []
date: 2023-08-03T02:40:27+05:30
lastmod: 2023-08-03T02:40:27+05:30
featured: false
draft: false

url_video: "https://youtu.be/wnMy73SlUnc?si=okSYs7X3cvBcP8zT"

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
I decided to create similar product like [VirusTotal](https://virustotal.com) . 

User will upload any file to [platfrom](http://ransomaware.xyz) that can be normal or malware file , then file/exe will excuted in virtual machine and cuckoo sandbox will generate behavioral analysis (activities, apicall's or system call by that exe file) and this analysis act as feature set for ML model and it will predict it is ransomware or normal file also provide log and dynamic analysis data . 

# Architecture 
Architecture we are goin to implement / follow 
![](Archi.png)



# Cuckoo Sandbox Installation video
I am aware that cuckoo sandbox is difficult to install due to huge dependency so i recorded the video for referance . 

{{% callout note %}}
Watch Cuckoo Sandbox Installation by clicking on Image 👇👇👇
{{% /callout  %}}
[![Watch the video](thumbnail.png!)](https://youtu.be/wnMy73SlUnc?si=okSYs7X3cvBcP8zT)
[![Watch the video](/project/dyanodaya/Home.png)](https://youtu.be/d_WhG0vqCr4)


### Referance Paper1 
Link of paper1 [https://ieeexplore.ieee.org/document/9536608](https://ieeexplore.ieee.org/document/9536608)

Paper In short : It classify the type of ransomeware family (out of 5 family used to train model ) from doing dynamic analysisi or observing paranoia activity / API calls . 

### Referance Paper 2
Link of paper [https://doi.org/10.1016/j.jksuci.2020.06.012](https://doi.org/10.1016/j.jksuci.2020.06.012)



We can also explore the hybrid approch i.e static and dynamic analysis to find ransomeware and then identify it's family . 