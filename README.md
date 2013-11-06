# htdocs-libregraphics-projects


List of free software and free projects for graphics. 

## Contributing

- For this repository, create a new branch, edit the files, make a pull request.
- Each directory contains one project:
  - `project/project.yaml` is a description with specific fields
  - `project/project.md` is a freeform description.
  - `project/project.png` is the bitmap logo.
  - `project/project.svg` is the svg logo.
  - `project/screenshot_00.png` is a set of screenshots.
- Each project should be described with one sentence (maximal length?) at the beginning of the markdown file. The rest of the file is free, but should be kept as short as possible and separated by level two (##) titles.
- Please do not mention the license nor the words "open source" nor "free" (as in software) in the description: all the software listed here is free and open source! please focus on what the software does for the user. And we have a "License" field for it in the yaml file.

## The `project.yaml` file

    name: <string>
    category:
        -  [bitmap|vector|dtp]
    type:
        - [software|community|news]
    latest release: <date>
    version: <string>
    active: <bool true>
    deprecated: <bool false>
    license:
        - [GNU GPL|BSD|Apache]
    site: <url>
    download:
        - platform: [Linux|MS Windows|Mac OS X]
          url : <url>
    repository: <url>
    mailing list: <url>
    forum: <url>
    programming language:
        - <C|C++|Python>
    tags:
        - <string>

No field is mandatory, but leaving out some fields (like the name) will result in the project not being displayed. Some fields have a default value (like "active").

## Todo:

- patch the markdown library to set the initial level of headings
- don't use `book.yaml`, but read each `project/project.yaml` file.
- check all licenses (remove GPL from the files where it's not for sure)
- rename GPL to GNU GPL
- fix the version and release field in all files.
- add a "deprecated" optional file
- find a way to add comments
- find a way to attach articles to each (multiple) projects. (in the yaml file? an article.yaml file?)
