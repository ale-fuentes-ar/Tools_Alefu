# tools : tmux
[ :running: to home][link-home]

![](https://img.shields.io/badge/by-Alejandro.Fuentes-informational?style=flat&logoColor=white&color=cdcdcd)

### Install and Execute
* Install

    ```bash
    sudo apt install tmux
    ```
* Executing

    ```bash
    tmux
    ```

### Using

**screen in tmux**

* split the screen in two verically: `CTRL + B` and after symbol `%` 
* navigate between the vertically screen: `CTRL + B` and right or left arrow.
* split the screen in tow horizontally: `CTRL + B` and after symbol `"`
* navigate between the horizontally screen: `CTRL + B` and up or down arrow.
* close screen: run command `exit`

**windows with tmux**

* for create a new windows: `CTRL + B` and after `c` key

In the left down corner, has information about what windows we has:

```
[0] 0:bash 1:bash*
```

in te example has two bash windows (`o:bash`, `1:bash`), and the second windows are show, I know it because tmux use `*` for indicate (`1:bash*`);

* for change between windows: `CTRL + B` and after number of screen (0, 1, so on)
* for change name os windows: `CTRL + B` and after comma `,`, next write name has we will want.
* for navigate trought screen (scrolling): `CTRL + B` and after `[` key. For exit press `q`.
* for close window: use command `exit`

**Session if a great featuren of tmux**

* for create the session: `CTRL + B` and after the key `d`
    ```
    [detached (from session 0)]
    ```
* for see the running in the background: the command `tmux ls`
    ```
    alefu@tortilla:~$ tmux ls
    0: 1 windows (created Thu Aug 25 19:01:19 2022)
    ```
* for attach again the session: the command `tmux attach -t 0`
* for rename session: the command `tmux rename-session -t 0 git`
    ```bash
    # listing sessions
    alefu@tortilla:~$ tmux ls
    0: 1 windows (created Thu Aug 25 19:01:19 2022)

    # rename the session
    alefu@tortilla:~$ tmux rename-session -t 0 git
    alefu@tortilla:~$ tmux ls
    git: 1 windows (created Thu Aug 25 19:01:19 2022)

    # attach the session before renaming
    alefu@tortilla:~$ tmux attac -t git

    ```
* for create a new session: the command `tmux new -s <name-session>`
    ```bash
    # listing my tmux sessions
    alefu@tortilla:~$ tmux ls
    0: 1 windows (created Thu Aug 25 20:09:34 2022)

    # rename session for a better identification
    alefu@tortilla:~$ tmux rename-session -t 0 git
    alefu@tortilla:~$ tmux ls
    git: 1 windows (created Thu Aug 25 20:09:34 2022)

    # create a new session for console
    alefu@tortilla:~$ tmux new -s docker

    # CTRL + B after 'd' key for save session
    [detached (from session docker)]

    # listing all tmux sessions
    alefu@tortilla:~$ tmux ls
    docker: 1 windows (created Thu Aug 25 20:10:40 2022)
    git: 1 windows (created Thu Aug 25 20:09:34 2022)
    ```
* how to finish o kill sessions: use command `tmux kill-session -t <name-session>`
    ```bash
    # listing sessions
    alefu@tortilla:~$ tmux ls
    docker: 1 windows (created Thu Aug 25 20:10:40 2022)
    git: 1 windows (created Thu Aug 25 20:09:34 2022)

    # killing one session indicating for him name
    alefu@tortilla:~$ tmux kill-session -t git

    # listing a verify that session are not exits
    alefu@tortilla:~$ tmux ls
    docker: 1 windows (created Thu Aug 25 20:10:40 2022)
    ```

    <!-- links -->
[link-home]: ../../README.md