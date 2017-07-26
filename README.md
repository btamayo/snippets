# snippets


## nix

users and groups:

```shell
$ sudo groupadd $NEWGROUP
$ sudo usermod -aG $GROUP $USER
```

symlinks:

```shell
$ ln -s <PATH TO REAL FILE> <PATH TO FAKE FILE>
```


ssh copy key using cat:

```shell
$ cat id_rsa.pub | ssh bianca@example.com "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"
```

---

## git 
git enable signing:
```shell
$ git config --local user.signingkey <key id or email>
```

git check if which branches are merged/not merged into master (or any branch):
```shell
$ git branch --no-merged master
$ git branch --merged master

```

---

## gpg

gpg exports:
- `-a` for ascii (armor) output

```shell
$ gpg --export-secret-keys -a YOURKEYIDORSOMETHING > secret.asc
$ gpg --import private.key
```


gpg decrypt:
```shell
$ gpg --output <OUTFILE> --decrypt --recipient <RECIPIENT> <INPUTFILE>
```

---

## docker

docker rmi:
```shell
$ docker rmi $(docker images -f dangling=true -q)
```