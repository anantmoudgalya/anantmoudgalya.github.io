---
layout: post
title: Internship Experience
---

This post details my internship experience @ [CimplyFive Secretarial Services Pvt Ltd.](https://www.cimplyfive.com/)

Hello Everyone! This post details what I had built during my 2 month (Jan-March 2020) period working as an intern for CimplyFive.
We were hired as a team of 2 interns (myself and [Ayman Shafi](https://www.linkedin.com/in/ayman-shafi-a2630b129/)) to work on a use case for the company. According to the Companies Act in 2013, companies in India are required to comply with certain regulations and compliances. So to streamline their process of doing so, CimplyFive offers a comprehensive web platform called BLISS, which can handle all the company's legal document needs in a nice GUI drag and drop interface and issue alerts when they're being non compliant.

As a part of BLISS, CimplyFive offers it's clients a service to digitise their 'Past Records'. That is, they physically scan the documents, classify them into necessary classes of meetings according to the Companies Act and upload them into the right financial year and meeting type onto BLISS. This is a labor intensive routine and our task was to automate this process and save valuable company time. (The application we built ended up completing what would've taken a week in manual effort in 5 minutes :D)

## Tasks Overview

We were given 2 tasks in the form of user stories. <br/>
<b>First</b>, to <b>classify documents</b> into their corresponding <b>meeting types</b> (Board Meetings, Shareolder Meetings etc) and their corresponding <b>file types</b> (Meeting Agenda file, Meeting Minutes files, Other pertinent files etc). Post classification these files were to be physically arranged in a specific directory structure to make it easier for domain users to check for correctness. We were also required to generate a classification report post classification to understand reason behind classification and erroneous classification, if any. <br/>
<b>Second</b>, to <b>upload these documents</b> according to their corresponding meeting types and financial years onto the company's BLISS portal and generate a detailed upload report.

## Technical Details

To parse and classify PDF documents, I used the Apache-Tika pdf parser's python wrapper, [Tika-Python](https://github.com/chrismattmann/tika-python). It can parse PDF files with great accuracy and proved to be the perfect choice for the requirement. <br/>
In order to store and query parsed pdf content, we had to make use of a document oriented database and build a text search engine around it. As the requirement needed the task to achieved with low overhead, I turned to a more pythonic way of building a document database, which was achieved with the help of [Whoosh](https://github.com/mchaput/whoosh). Whoosh helped us store parsed document content in a lightweight form using few temporary files. <br/>
It has extremely fast indexing capability and I observed it to index over 100 documents within a minute of time. Whoosh also had a full text search capability which I augmented with a custom scorer as per classification requirments. I also used Python's standard os module to move files around and create the desired file structure and used the Python CSV module to generate the classification report. <br/>
For the purpose of upload, I used a series of RESTful API calls, back and forth from BLISS using the Python [Requests](https://requests.readthedocs.io/en/master/) library. To necessitate easy reading and understanding of the upload of over hundreds of documents to both domain users and clients, I was required to automate the building of a very detailed upload report. This was done using the [XlsxWriter](https://xlsxwriter.readthedocs.io/) plugin for Python and helped me generate color coded reports which were appreciated by the domain users at the company.  During the process, I also learnt about how to store and process data efficiently in program memory and make the use of data structures to do so. <br/>
We built a standalone desktop application with a [tkinter](https://docs.python.org/3/library/tkinter.html) GUI and built the modules together into an executable, with the help of the [PyInstaller](https://www.pyinstaller.org/) module. To automate the building process after bug fixes we used Github [Actions](https://github.com/features/actions) to facilitate the application build on push to the code repository.

## Major Takeaways

I learnt how to dissect user stories into tangible research tasks, modularizing your code, test automation, logging, reporting etc. I also learnt a lot of valuable lessons with respect to the software development lifecycle. I would like to thank CimplyFive for this opportunity. More importantly, I would like to thank my mentor and the CTO of CimplyFive, [Roshan Hadal](https://www.linkedin.com/in/roshanhadal/) for showing faith, for being supremely kind, patient and teaching a lot of invaluable lessons. <br/>
<b>I wish CimplyFive all the best!</b>