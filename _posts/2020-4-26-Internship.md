---
layout: post
title: Internship Experience
---

This post details my internship experience @ [CimplyFive Secretarial Services Pvt Ltd.](https://www.cimplyfive.com/)

Hello Everyone! This post details what I had learnt during my 2 month (Jan-March 2020, May 2020 - Present) period working as an intern for CimplyFive.
We were hired as a team of 2 interns (myself and [Ayman Shafi](https://www.linkedin.com/in/ayman-shafi-a2630b129/)) to work on a use case for the company. The use case is a labor intensive routine and our task was to automate this process and save valuable company time. 
(The application we built ended up completing what would've taken a few days in manual effort in 5 minutes :D)


## Technical Takeaways

* I learnt about automating PDF parsing, i.e, extracting text from pdf files. I used the Apache-Tika pdf parser's python wrapper, [Tika-Python](https://github.com/chrismattmann/tika-python). It can parse PDF files with great accuracy and proved to be the perfect choice for the requirement. <br/>
* I became competent with NoSQL, document oriented databases and learned about building a text search engine around it. I became proficient with MongoDb and it's text search capability. To accomplish the text search with lower overhead, I found a more pythonic way of building a document database, which was achieved with the help of [Whoosh](https://github.com/mchaput/whoosh). Whoosh helped index and store parsed document content in a lightweight form using few temporary files in a very short time. <br/>
* It has extremely fast indexing capability and I observed it to index over 100 documents within a minute of time. Whoosh also had a full text search capability which I augmented with a custom scorer to perform rank based search. I also acquainted myself with folder traversal and modifying directory structures using the python OS module.<br/>
* I acquired skills pertinent to RESTful API calls, acquainting myself with this brilliant piece of software called Postman. Postman provides wonderful utility for imitating API calls and observing GET/POST results, headers etc. I administered a bunch of RESTful API calls using the Python [Requests](https://requests.readthedocs.io/en/master/) library. 
I also became proficient with automating the writing of reports for Domain users. This was done using the [XlsxWriter](https://xlsxwriter.readthedocs.io/) plugin for Python and helped me generate color coded reports which were appreciated by the domain users at the company. 
* During the process, I also gained an understanding of how to store and process data efficiently in program memory using hashmaps, tree structures, JSON files and python lists to do so. <br/>
* We built a standalone desktop application with a [tkinter](https://docs.python.org/3/library/tkinter.html) GUI and built the modules together into an executable, with the help of the [PyInstaller](https://www.pyinstaller.org/) module. 
* To automate the building process after bug fixes we used Github [Actions](https://github.com/features/actions) to facilitate the application build on push to the code repository. GitHub Actions were a very stimulating study as watching a release artifact get built automatically on push to the Master repository was wonderful to see happen.

## Non Technical Takeaways

* I learnt how to dissect user stories into tangible research tasks, modularizing your code, test automation, logging, reporting etc. 
* I picked up a lot of valuable lessons with respect to the software development lifecycle and about organizing tasks according to business priority. 
* Teamwork. Working as a part of team, and taking everyone's opinion constructively and adding it to my knowledge base was a valuable lesson. 
* Professional Communication and Networking helped me foster necessary skills to improve as a professional.
* More importantly, I learnt about taking criticism constructively and using it to improve my work. I also learnt about Time Management, as a student, it is easy to fall to the habit of procrastination. But in a professional setting, I was pushed to use my time efficiently and work better.