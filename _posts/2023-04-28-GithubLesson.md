---
toc: true
comments: true
layout: post
title: April 28 Github Lesson
description: Includes all the important stuffs about Github and Git
---

Why Github?

- Github is a website used to share coding repositories.
- Github is integrated with Git, which is used for coding repositories. Better than Google Drive
- Git is different from Github as Git is a way to store code and there are commands. Github is the website used to share code.

Git commands
- git clone
- git push
- git config
- git add
- git branch
etc

Which is better, MacOS or windows?
- Windows: More compatible for downloads
- MacOS: ????

But neither is actually better!

List of tools
- VSCode: Syncs to Github. Good for development
- Kernels: Required to run the code

Installations was hard the first time since it was the beginning (it was hard)
- Things got easier as we got used to them (recognizing error messages)


More git commands
- git fork - make your own copy of someone's repository
- git checkout - commit to a test branch (not the main branch)



### Notes on frontend and backend

CRUD - create, read, update, delete

Create: Make new entries to database
Read: Get info from database
Update: Overwrite data from database
Delete: Remove data

Films API: LIst of fillms someone watched

Includes youtube trailer, episode, etc.

Create: Makes films
Read: Returns films
UPdate: New episodes
Delete: Deletes films


Note: CRUD was integrated into frontend

Example was given for home alone in [API](https://tanayp327.github.io/Quintic5/films.html)

Scripts
- Takes URL of localhost to create, update, delete, etc.

ConverttoEmbedUrl function
To embed a Youtube Video in HTML, you need an embed link. String manipulation is used to change the usual URL to the embed URL.

CRUD - name, year, language, etc.
- Gets all the attributes for create

Delete has 2 options
- Delete 1
- Delete All

Update
- Can add new episodes (in case a show is ongoing)

Cleaning (garbage checking)
- Input boxes: Should have at least 2 characters
- Year: After 1800, should be a number
- List: AT least 1 element
- Trailer: Error handling with rickroll as placeholder


Fetching (from 3rd party API)

- Retrieve data from server/database
- GET/POST/PUT/DELETE or HTTP methods
- Can use AJAX, etc. Use FETCH API
- Sends request to server using URL with location of what is requested 
- Can do formats (JSON) allowing for easy JS manipulation
- Use Pandas to make the data readable in a dataframe
