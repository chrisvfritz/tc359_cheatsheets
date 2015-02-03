*Tested on Linux. Mac users might be able to follow suit too. Windows users, make a Linux virtual machine.*

1. When bash starts, it looks in your home directory for the files `.bashrc`, `.bash_profile`, and `.profile`. If they exist, it will run the commands in each one it finds.

2. The `alias` command is one of bash's greatest timesavers. Here's an example you can type into your shell: `alias bye='sudo shutdown -h'`*. From then on until the shell is closed, any command beginning with (or containing only) "bye" will have that word substituted for the alias you just defined. Used in an example:

``` bash
[19:38 ~/tc359/cheatsheets/misc] % bye 50

Broadcast message from ec2-user@ec2-host
    (/dev/pts/0) at 19:38 ...

The system is going down for halt in 50 minutes!

```
You could've written `sudo shutdown -h 50`, but you didnt' didn't have to. Sixteen keystrokes reduced to three.

3. The command to push to GitHub, generally speaking, is `git push origin`. 

4. Likewise for Heroku, it's `git push heroku`.

5. Bring the four above facts together for one huge tip:
``` bash
[19:49 ~/tc359/cheatsheets/misc] % cd ~
[19:49 ~] % echo "alias megapush='git push origin && git push heroku'" >> .profile
[19:49 ~] %
```
Call it whatever you want, but I called it "megapush". Here's a copy-pasteable version:
``` bash
cd ~
echo "alias megapush='git push origin && git push heroku'" >> .profile
```

Now every time you open bash, it'll run `alias megapush=...`. This will allow you to just type `megapush` and push to GitHub and Heroku at the same time.

\* `sudo` elevates a command to administrator level. `-h` stands for "halt", meaning "power the system off after shutdown". `shutdown` demands a time value, which can be expressed in minutes (or `now`).

Further reading:
- https://www.digitalocean.com/community/tutorials/an-introduction-to-useful-bash-aliases-and-functions
