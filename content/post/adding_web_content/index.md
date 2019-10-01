---
title: Adding Content (e.g. protocols/blog posts) to the Lab Website 
featured: true
authors:
- jesse
date: 2019-09-13
---

## Preamble:

At first, this may seem like an excessively complicated way of updating a website, but it actually will teach you how to use github. By the end of it you should be able to clone, fork, and merge like a pro!

## Dependencies:

* Github (for pushing, pulling, etc) - make sure you're also a member of "fuhrman-lab" group on github
* [Hugo](https://gohugo.io/) (for generating a html website from markdown content)

## Instructions:

1. Go to [github](https://github.com), make sure you're logged in. 
2. Once you're logged in, go to our "group" account https://github.com/fuhrman-lab
3. Find the "academic kickstart" repository and click "fork" at the top of the page. (This creates a copy of this repository that you can work and play with locally on your own machine. You can make any changes you want, test to see how they'll look on the website, then once you're satisfied we'll "pull" those changes back into the "master" branch of our group account.)
4. It's probably a good idea to go to "settings" and rename it to something like "academic-kickstart-fuhrmanlab" because you may also want to use the same framework to create your own website later on and it's confusing if they're named something similar like "academic-kickstart-1" and "academic-kickstart".
5. Now that you've got this on your account, clone it locally:
e.g. `git clone git@github.com:fuhrman-lab/academic-kickstart.git Fuhrman_Lab_Website/` #Make sure to use the ssh cloning option (not https), if not you'll have to change it later to use ssh authentication\*
Note that your destination folder (named `Fuhrman_Lab_Website` above is your **base repository** for later steps.
6. Enter the folder and run the following command:
`git submodule update --init --recursive`
7. Test to make sure hugo is working. Run the following **from the base directory of your repository**:
`hugo` #should create a "public" directory. This is basically taking all the markdown etc and making it into html
`hugo serve`
The latter command will set up a local webserver which should listen for changes. So you can play around and then switch to your browser to see how the changes look. Just open the website address your terminal provides. You can keep this terminal open while you edit other files.
8. The first thing you want to set up is a profile for yourself as an author. Go to `content/authors` and create a new folder for yourself. You can just copy someone else's folder as follows:
`cp -r jesse yourname`
Then just go in and edit the content in the markdown (.md) file. You can replace avatar.jpg with your picture if you want. Add your twitter handle, google scholar, github etc and a small blurb about yourself. That way, when you post something there will be a profile associated with it and people can read about your research etc.
9. Now we can add some content! To make it easier for others in the lab to follow, please provide a blog post-like description of the background behind the protocol as well as a link to a PDF or website where the protocol is stored. To make a new post, just copy one of the existing folders in the same way you ddid for your profile, and edit the markdown to create your post. PDFs and other files can be stored in this folder too, and I like to put them in a 'files' subfolder to keep it organized. It then can be linked in your post as follows: `[Text you want to show](files/testing.pdf)`, which will render like this: [Text you want to show](files/testing.pdf)
10. Take a look at your post in your local browser instance, and edit until you think it looks good!
11. Remove any subfolders called `public`, which may appear in folders you have modified, e.g. `rm -rf public`.
12. Now we're ready to push the changed content to the remote repository. What we're going to push is the markdown content but not the hugo-generated website in the "public" folder. In academic-kickstart this is already taken care of by the addition of a .gitignore file. Take a look at it yourself to see how it works - this will probably come in handy in your future work.
13. OK so we gotta do three things: add, commit and push, as follows (make sure you do this from your repository's **base directory**):
`git add .` #adds everything

`git commit -m "Adding instructions for updating website"` #change message to explain what you've done

`git push origin master` #sends your changes to the interwebs

14. The rest is easy! Go to your **academic-kickstart-fuhrmanlab** repository, and make sure the changes have been successfully pushed. You should see some files have been changed recently, and also that your branch should be several commmits ahead of the fuhrman-lab master branch. Once you've confirmed this, then initiate a pull request. Follow the prompts, add in any relevant info, and then likely you can automatically merge it with the master branch (we're all part of the same group so we all have access). Once this is done, then just let Jesse know and he can update the website!

\* e.g. `git remote set-url origin git@github.com:fuhrman-lab/academic-kickstart`
