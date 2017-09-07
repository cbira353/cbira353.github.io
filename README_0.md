# README cbira353.github.io

How to update the Portfolio Website in cbira353.github.io hosted by repository Git Pages

## Where to find the Portfolio Site directories

go to `Dropbox/Sites/cbira353@github.com`

then only change the following files and directories:

## Tree
scan the directory structure: `tree` or `tree -Q -L 1` for first level directories
 
## Where the important directories are

### Site Content: articles and blog directories
All of Blog site content in .md are placed here.  From these .md pages are created the .html files for the portfolio site.

```
├── _posts
│   ├── articles  >> where the .md files for HOW TOs are
│   └── blog >> where my MUSINGS are
```

### Jekyll-generated HTML files
Where the Jekyll-generated site HTML files are located. DO NOT TOUCH THESE FILES
```
├── _site
│   ├── about
│   ├── articles
│   ├── assets
│   ├── blog
│   ├── css
│   ├── images
│   ├── learning,
│   ├── photos
│   ├── search
│   ├── tags
│   └── theme-setup

```

#### Holding pen for drafts of content

`├── _drafts `

#### Add .jpg or .png files in the `├── _images ` 
Remember to ignore the `├── photos ` directory, as this is used by Jekyll
The index.md file is generated and tells Jekyll where the images' urls are:

```
---
layout: photos
modified: 2016-09-26
images:
  - image_path: /images/archway.jpg
    title: Archway
  - image_path: /images/big-ferns.jpg
    title: Big Ferns
  - image_path: /images/ricefield.jpg
    title: Rice Field
  - image_path: /images/sprite.jpg
    title: Pan
  - image_path: /images/buddha.jpg
    title: Big Buddha
  - image_path: /images/japanese-banner.jpg
    title: Festival Banner
  - image_path: /images/japanese-lady.jpg
    title: Japanese Lady
  - image_path: /images/japanese-house.jpg
    title: Japanese House
  - image_path: /images/grasshopper2.jpg
    title: Grasshopper
  - image_path: /images/market.jpg
    title: Open Market
  - image_path: /images/rain.jpg
    title: Rain in the Tropics
  - image_path: /images/fall-in-bbrae.jpg
    title: Fall
  - image_path: /images/hongkong-cleaning.jpg
    title: Street Cleaning - Hong Kong
  - image_path: /images/hk-tugboat.jpg
    title: Hong Kong Tugboat
  - image_path: /images/enzo.jpg
    title: Enzo
---


<ul class="photo-gallery">
  {% for image in page.images %}
    <img src="{{ image.image_path }}" alt="{{ image.title}}">{{ image.title}}
    <br><br>
  {% endfor %}
</ul>
```

## Make changes to the local directory

To display locally change `_config.yml`, swapping between the two. Make sure you comment out one of them.
```
#url: "http://localhost:4000"
url: "https://cbira353.github.io"
```

## To start the Jekyll server enter the following:

`bundle exec jekyll serve`

To *stop server*: `Ctrl + C`


## Viewing via local server:

Open SublimeText and make changes in the proper file
When wanting to view on local browser, do the following:

```
Shft + Ctrl P  # to find the Markup Viewer
```
Choose "Markdown Preview > Preview in Browser"
Find the open Browser window displaying the latest changes in the local directory

## Git 
Make sure in synching local vs remote, you `git push` often:

`git status`
`git add .`
`git commit -m 'Some comment`
`git push origin master`

You will then be challenged by github:
```
mbira@tchotchke:~/Dropbox/Sites/cbira353.github.io$ git push origin master
Username for 'https://github.com': YOUR USERNAME
Password for 'https://cbira353@github.com': YOUR PASSWORD

Counting objects: 4, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 372 bytes | 0 bytes/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/cbira353/cbira353.github.io.git
   ee8a4a9..f0c371b  master -> master
```


## Adding a new Menu Tab item and directory changes
_to be added next time_


That's it for now.