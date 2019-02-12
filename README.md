# The Downs Is Here Official Guide
Follow this guide as closely as possible and if you run into an error contact me.

## Installation
Install [git](https://git-scm.com/downloads). Follow the installer defaults, that stuff doesn't matter. This is the piece of software that takes the files from your computer and puts them on the internet.

Next, download and install (Visual Studio Code)[https://code.visualstudio.com/download]. This is the editor that you will use to edit your blog. While it is slightly more difficult than using a platform like Weebly or WIx this is better.

## Setup
Next, create a folder in a directory somewhere, it doesn't matter where. Name this folder `blog`. Now, click in the file bar of the Windows Explorer and type `cmd` then press enter. A window called the *Terminal* will open. On the left, you will see the directory you opened this Terminal from.

Now, type the following command, pressing enter afterwards:
`git clone https://github.com/downsishere/downsishere.github.io.git` this command downloads your website from GitHub so you can edit it. You'll only have to do this one time.

Next, open the folder `blog/downsishere.github.io` in Visual Studio Code by using the `File > Open` menu.

## Editing Your Blog
In Visual Studio Code, the top icon in the sidebar (Explorer) shows you a list of the files in this project. Click this. The posts you will write go under the `blog/downsishere.github.io/_posts` directory. There is already a file in this folder, copy it and edit when you want to make a new post.


## Publishing Your Blog
Click the third icon in the sidebar of Visual Studio Code (Source Control). Here you will see a list of all the changes that you (and the software) have made. Follow the steps below:
1. Hover over the **CHANGES** title to see a **+** icon appear. Click it and see the **CHANGES** title change to say **STAGED CHANGES**. 
2. In the textbox that says "Message (press Ctrl-Enter)" type a message (it can be anything) and press `Ctrl-Enter`.
3. Click the three horizontal dots in the top then click Push.
4. Your website is now live at [downsishere.github.io](https://downsishere.github.io)
