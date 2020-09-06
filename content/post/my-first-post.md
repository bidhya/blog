---
title: "Github user page using Hugo on Windows"
date: 2020-08-27T14:10:52-04:00
tags: ["tag1"]
categories: ["cat2"]
---
Since most of the online instruction for Hugo was related to Mac/Linux, I decided to write post for my own sanity!  

Change1  

1. Download Hugo executable from this [site](https://github.com/gohugoio/hugo/releases)
    - Unzip and put on any folder
    - Set path to to this exe file so that you can start using hugo command from any folder location

2. Create Hugo Project  
    - hugo new site blog  
    - cd blog  
    - git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke

3. Configure the site  
    Change the config.toml as follows:  
    - baseURL = "https://bidhya.github.io/"
    - languageCode = "en-us"
    - title = "Bidhya N Yadav"  
    - theme = "ananke"  
4. Write your post/blog  
    * hugo new post/my-first-blog.md  
    * Edit this blog on your favorite editor (eg: Visual Studio Code)  

5. Version control with github  
    - git init   
    - git add --all  
    - git commit -m "Initial commit for blogging"  

    Add remote repo
        Create a new github project, say blog, for example
        git remote add origin https://github.com/<USERNAME>/blog.com.git

6. Add github.io page  
    First create bidhya.github.io page on remote  
    On local machine:  
        git submodule add -b master https://github.com/<USERNAME>/<USERNAME>.github.io.git public .  
        Make sure base url on config points to this site  

7. Generate webpages with HUGO
            hugo  
            cd public  
            git add --all  
            git commit -m "generating web pages"  
            git push origin master  

8. Add pages and update as follows
    hugo
    cd public
    git push

Note:
    Add .gitignore inside the blog repo and add `public/`  
    That way public pages are not hosted on blog repo

Notes Specific to Hugo
archetypes: to define frontmatter templates
shortcodes: predefined html that can be inserted into md file
taxonomies: tags inside the fornt matter or categories

