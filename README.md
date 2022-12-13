# GITHUB MANUAL

This repository is for handling about GIT.
You can learn about how to use github. I have maded course for how to study about git and it's features step by step.
There would be kind explanations of every each of terms. THANK YOU!

## Preparation ##

- GIT 다운로드
download links : https://git-scm.com/downloads

본인에게 알맞는 OS버전의 깃을 다운로드하여 설치.

----------------------------------
# 깃을 시작해보자

'git' 을 터미널 또는 gitbash 에서 입력.

```
user Desktop64 ~ 
$ git
```
정상적으로 설치가 완료되었다면 아래와 같은 정보 출력
```
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects
```

## 1. git init

'init' 명령어는 현재 디렉토리를 git의 작업 장소로 설정.
- 예제
1. 임의의 디렉토리 하나 생성.
2. 생성된 디렉토리로 이동
3. ```git init``` 명령어 입력
해당 디렉토리가 git의 작업 장소로 설정되며 추가적으로 ```./git``` 이라는 디렉토리가 생성된다.
```.git/``` 딜게토리 안에는 작업장소에 관련한 다양한 정보와 특징 그리고 버전이 저장되어 있다.

## 2. git add
-예제
git init 과정에 이어서 시작.
1. 생성된 디렉토리에 ```file1.txt``` 파일 생성.

file1.txt 내용
```
code1
```



   
   
