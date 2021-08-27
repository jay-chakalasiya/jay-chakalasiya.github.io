This repository is for my blog, where I actively share ideas and projects, visit the live deployed version at [jay-chakalasiya.github.io](https://jay-chakalasiya.github.io).

# Description

I'm passionate about Machine Learning and Artificial Intelligence; I spent most of the time exploring and learning new things. This blog is a way to communicate my knowledge.

I'm trying to post at least once a week, but sometimes it takes longer because of the busy schedule. I'm the sole contributor to this repository, if you find any conflicts or have any suggestions, please reach out to me at <chakalasiyajay00@gmail.com>

# Deployment

If you like the template and want to make a similar website, There are two ways to do it.
- Fork this repository and rename the repo to `<YOUR GITHUB USERNAME>.github.io`. 
- Or you can clone it locally and then add the files to `<YOUR GITHUB USERNAME>.github.io`. 
## Running it locally

This site is made using [Jekyll](https://jekyllrb.com/) blogging platform, using [Minimal-Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme. Jekyll works on [Ruby](https://www.ruby-lang.org/en/). Although editing this site locally doesn't require to know ruby, some installation is needed. Follow the steps below, or you can also look at Jekyll documentation
- Clone this repository at your desired location using this command
    ```bash
    git clone https://github.com/jay-chakalasiya/jay-chakalasiya.github.io.git
    ```
- Install Jekyll - follow the [Official Documentaion](https://jekyllrb.com/docs/). 
    - I used ruby 2.6.0, the newer versions might work, but I recommend going with the same settings if you don't have experience with ruby or Jekyll.
- Go to the root of the cloned repository and run the below command. It will install all the required packages.
    ```bash
    bundle install
    ```
- Run the command below. Now, most probably, you can see your deployed version at [localhost:4000](http://127.0.0.1:4000)  or follow the instructions on the terminal.
    ```bash
    bundle exec jekyll serve
    ```

## Structure/Files:
```
Root
|   .travis.yml                       # You need this file to make domain-related changes
|   Gemfile
|   index.html
|   package.json
|   README.md
|   _config.yml                       # This is an essential file and has global settings
|         
+---assets
|   +---images
|   |                                 # All the images go here 
+---_data
|       authors.yml
|       navigation.yml
|       ui-text.yml
|   +---footer
|   |       custom.html
|   +---head
|   |       custom.html
+---_layouts
|       archive-taxonomy.html
|       archive.html
|       categories.html
|       category.html
|       collection.html
|       compress.html
|       default.html
|       home.html
|       posts.html
|       search.html
|       single.html
|       splash.html
|       tag.html
|       tags.html
+---_pages
|       404.md
|       about.md
|       pages_archive.md
|       posts_category_archive.md
|       posts_tag_archive.md
|       project_archive.md
|       sitemap.md
+---_posts
|       2020-11-16-How-to-Use-Jekyll-Posts.md
+---_projects
|       new-file.md                  
            
```

# Licenses
This repository is licensed under MIT license, I have modified the [Minimal-mistakes](https://mmistakes.github.io/minimal-mistakes/) theme for the purpose; all the usage permits can also be found under [base_code_licenses](https://github.com/jay-chakalasiya/jay-chakalasiya.github.io/tree/master/_base_code_licenses).

Feel free to reach out to me on <chakalasiyajay00@gmail.com> in case of attributions or license conflicts.

# Contribute
If you fork and make some significant design changes, please send a merge request, I will be happy to add you as a contributor as well.

Or If you have some exciting post to share, feel free to reach out, I can create an author profile and publish your posts.

Regarding any suggestions or problems in blog content, the best way to react is using the comment section below the post.
