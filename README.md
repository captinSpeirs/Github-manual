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
```.git/``` 디렉토리 안에는 작업장소에 관련한 다양한 정보와 특징 그리고 버전이 저장되어 있다.

## 2. git add
-예제
git init 과정에 이어서 시작.
1. 생성된 디렉토리에 ```file1.txt``` 파일 생성.

- file1.txt 내용
```
source1
```

2. ``git status`` 명령어 입력

다음과 같은 정보 출력이 된다.
```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   f1.txt

no changes added to commit (use "git add" and/or "git commit -a")
```
``f1.txt`` 파일이 git의 작업 목록에 트랙킹(tracking) 되지 않는 다는 뜻이다. git 작업소에서 작업을 하면서 변경된 파일 또는 새로 생긴 파일들은
작업하면서 변경이 되었기 때문에 ``git init`` 을 통해 버전관리가 되고 있는 디렉토리안에 존재하지만 해당 파일이 git에게 버전관리 목록에 포함하기
위한 명령을 내리기 전까지는 해당 파일을 무시한다.

3. 해당 파일을 작업 목록에 포함시키기 위해서는 ``git add filename`` 을 입력한다.
``git add f1.txt``

4. 3번을 실행 하고 난 후, ``git status`` 를 입력하면 해당 파일이 트래킹이 잘 되었다는 정보 출력을 받을 수 있다.
```
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   f1.txt
```

## 3. git status
현재 git 의 상태를 확인.





   
   
