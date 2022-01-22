# Easy to use MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).


## 1. Follow the MkDocs docs to install 

These are some usedful commands bellow, 

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## 2. Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
        
## 3. Import to Github 

- Type `mkdocs serve` in your local terminal; you can preview the docs website.
- I push my local files (create by using `mkdocs new [dir-name]` commands) to Github by the [**Github desktop**](https://desktop.github.com/). There are a lot of ways to push them.

## 4. Deploy by **Read the Docs** (And some remarks)
- Then deploy the website by [Read the Docs](https://readthedocs.org/). You need to log in and import your repo from GitHub, then click `build.` I think the procedure is even easier than using [Netlify](https://www.netlify.com/).
- Let's talk about **plugins**. I have errors many times almost forgive using plugins like importing jupyter notebook (.ipynb) -- that is a dream function to me! I searched for so many ways to deploy my coeds in jupyter notebook easily, and I found this plugin! I tried it at local can work, But when I deployed to Read the Docs, it couldn't build.  
- For solving the error, you need to follow the [docs](https://docs.readthedocs.io/en/stable/config-file/v2.html#mkdocs) of readthedocs, create a `.readthedocs.yaml` in your repo. You just need to copy and paste these codes below. But the question is, what things do I have to write in the `requirements.txt` file?? 


```
python:
   install:
   - requirements: docs/requirements.txt
```

- The answer is to type the things you need to install (as well as in your local environment). For example, I need to install the package `mkdocs-jupyter` (at the file `readthedocs.yaml`) for using the plugin `mkdocs-jupyter` (at the file `mkdocs.yml`), so I just type `mkdocs-jupyter` in the `.txt` file. Then it can work.



