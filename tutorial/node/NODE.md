# NODE JS :: what is
[ :running: to home][link-home]

![](https://img.shields.io/badge/by-Alejandro.Fuentes-informational?style=flat&logoColor=white&color=cdcdcd)
![](https://img.shields.io/badge/tool-NodeJS-informational?style=flat&logo=node.js&logoColor=white&color=339933)



**Install in Ubuntu 20.04 LTS**

* first time, update our system
    ```shell
    sudo apt update
    ```

* second time, install package of node

    ```shell
    sudo apt install nodejs
    ```

* finish, testing version the our `nodejs`

    ```shell
    node -v
    ```

* for install npm, node package manager:

    ```shell
    sudo apt install npm
    ```

## Node Version Manager. 

[NVM][link-mvn] allows you to install and maintain many different independent versions of Node.js, and their associated Node packages, at the same time.

* first, install using `curl`:
    ```shell
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
    ```

* for install in our user account:
    ```shell
    source ~/.bashrc
    ```

* some commands:
```shell
# listing remote version
nvm list-remote

# install one version
nvm install v18.12.1

# listing all version installed
nvm list

# for use node system version
nvm use system

# install default
nvm install lts/fermium

mvn list
# output
->     v14.21.2
         system
default -> lts/fermium (-> v14.21.2)
iojs -> N/A (default)
unstable -> N/A (default)
node -> stable (-> v14.21.2) (default)
stable -> 14.21 (-> v14.21.2) (default)
lts/* -> lts/hydrogen (-> N/A)
lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.17.1 (-> N/A)
lts/carbon -> v8.17.0 (-> N/A)
lts/dubnium -> v10.24.1 (-> N/A)
lts/erbium -> v12.22.12 (-> N/A)
lts/fermium -> v14.21.2
lts/gallium -> v16.19.0 (-> N/A)
lts/hydrogen -> v18.12.1 (-> N/A)


# set default
nvm use v14.10.0

node -v
# output
v14.10.0
```

## Uninstall

```shell

# uninstall node
sudo apt remove nodejs

sudo apt purge nodejs

# uninstall nvm
nvm current

nvm uninstall <node_version>

nvm deactivate
```

<!-- links -->
[link-home]: ../../README.md

[link-mvn]: https://github.com/nvm-sh/nvm