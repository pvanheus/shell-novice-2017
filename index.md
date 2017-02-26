---
layout: lesson
root: .
---

The Unix shell has been around longer than most of its users have been alive.
It has survived so long because it's a power tool
that allows people to do complex things with just a few keystrokes.
More importantly,
it helps them combine existing programs in new ways
and automate repetitive tasks
so they aren't typing the same things over and over again.
Use of the shell is fundamental to using a wide range of other powerful tools
and computing resources (including "high-performance computing" supercomputers).
These lessons will start you on a path towards using these resources effectively.

> ## Prerequisites
>
> This lesson guides you through the basics of file systems and the
> shell.  If you have stored files on a computer at all and recognize
> the word “file” and either “directory” or “folder” (two common words
> for the same thing), you're ready for this lesson.
>
> If you're already comfortable manipulating files and directories,
> searching for files with `grep` and `find`, and writing simple loops
> and scripts, you probably won't learn much from this lesson.
{: .prereq}

> ## Getting ready
>
> This lesson will be run on the SANBI computer cluster and you will need to be able to log in there.
> The machine you need to log into is called *training.sanbi.ac.za*. You need to know
> you username - the instructor will tell you what it is. To log on, in the *terminal*
> type the command:
>
> ~~~ {.input}
> ssh username@training.sanbi.ac.za
> ~~~
>
> where **username** should be the username you have been allocated e.g. **emily**.
> The first message you see might be like this:
>
> ~~~ {.output}
> The authenticity of host 'training.sanbi.ac.za (192.168.2.101)' can't be established.
> RSA key fingerprint is SHA256:WA0/wLOhnSuVjaV5mZ/WQ2FHPWP3VyXAXsNybbvcPQM.
> Are you sure you want to continue connecting (yes/no)?
> ~~~
>
> If the *RSA key fingerprint* corresponds with what is shown above answer **yes** and
> press *Enter*. You will only get this warning message the first time you log in to
> *training.sanbi.ac.za*. You will now be asked for your password:
>
> ~~~ {.output}
> username@training.sanbi.ac.za's password:
> ~~~
>
> Enter the password for your account and you should see something like this:
>
> ~~~ {.output}
> Welcome to Ubuntu 16.04.2 LTS (GNU/Linux 4.4.0-64-generic x86_64)
>
>  * Documentation:  https://help.ubuntu.com
>  * Management:     https://landscape.canonical.com
>  * Support:        https://ubuntu.com/advantage
>
> 0 packages can be updated.
> 0 updates are security updates.
>
> Last login: Sun Feb 26 11:02:41 2017 from 192.168.2.42
> username@training:~$
> ~~~
>
> This **username@training:~$** is the *command prompt*. If you see this,
> you are ready to proceed. In the examples this prompt is shown as **$** for brevity. Once you are logged in:
>
> 1. Unzip/extract the data we will be working with using the **unzip** command:
>
> ~~~ {.input}
> $ unzip /opt/shell-novice-data.zip
> ~~~
>
> This will unpack the data into a directory *data-shell* in your home directory.
> In the lesson, you will find out how to access the data in this folder.
