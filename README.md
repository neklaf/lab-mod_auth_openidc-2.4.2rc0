# lab-mod_auth_openidc-2.4.2rc0
https://github.com/zmartzone/mod_auth_openidc/commit/f6798246abc8fd8f865db313439882ac9f5771f3

## How to build Apache Openidc module on Debian GNU/Linux
These are the steps I've followed to build that fix on Debian GNU/Linux Bullseye:

### Install dependencies:
```
# apt update
# apt install apache2-dev
# apt install libcurl4-openssl-dev
# apt install libjansson-dev
# apt install libcjose-dev
# apt install libhiredis-dev
```
From this point you could clone the repository:
`$ git clone https://github.com/zmartzone/mod_auth_openidc.git`

Or if you need compile a specific commit you could follow the steps explained in the following section.

### Download a specific commit from github:
In this case we would like to download a specific commit from the Apache module repository, specifically the following one:
[https://github.com/zmartzone/mod_auth_openidc/tree/f6798246abc8fd8f865db313439882ac9f5771f3](https://github.com/zmartzone/mod_auth_openidc/tree/f6798246abc8fd8f865db313439882ac9f5771f3)

If the repository is in github, you can navigate to the tree view of that repository at [https://github.com/<repo_name>/tree/<commit_sha>](https://github.com/<repo_name>/tree/<commit_sha>)
Then clicking on the Download ZIP button on the right-hand navigation bar will download the source code to the specified commit.
```
$ unzip mod_auth_openidc-f6798246abc8fd8f865db313439882ac9f5771f3.zip
# cd mod_auth_openidc-f6798246abc8fd8f865db313439882ac9f5771f3
```

### Compiling Apache Openidc module
These are the commands required to build the module:
```
# ./autogen.sh
# ./configure
# ./make
# ./make install
```

### References
[https://coderwall.com/p/xyuoza/git-cloning-specific-commits](https://coderwall.com/p/xyuoza/git-cloning-specific-commits)
