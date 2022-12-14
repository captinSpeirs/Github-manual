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

예제

**1.** 임의의 디렉토리 하나 생성.

**2.** 생성된 디렉토리로 이동

**3.** ```git init``` 명령어 입력

해당 디렉토리가 git의 작업 장소로 설정되며 추가적으로 ```./git``` 이라는 디렉토리가 생성된다.
```.git/``` 디렉토리 안에는 작업장소에 관련한 다양한 정보와 특징 그리고 버전이 저장되어 있다.

## 2. git add
-예제
git init 과정에 이어서 시작.

**1.** 생성된 디렉토리에 ```file1.txt``` 파일 생성.

- file1.txt 내용
```
source1
```

**2.** ``git status`` 명령어 입력

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

**3.** 해당 파일을 작업 목록에 포함시키기 위해서는 ``git add filename`` 을 입력한다.
``git add f1.txt``

**4.** 3번을 실행 하고 난 후, ``git status`` 를 입력하면 해당 파일이 트래킹이 잘 되었다는 정보 출력을 받을 수 있다.
```
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   f1.txt
```
해당 정보에서 modified 라는 정보를 확인 할 수 있다.
modified : 변경된 파일
new file : 새로 만들어진 파일

## 3. git status
현재 git 의 상태를 확인. 

## 4. git commit
깃에 변경된 사항이 생기고 해당 변경 부분을 ``git add`` 명령어를 통해 트래킹하고, 확인(confirm) 작업을 한다.
이를 통해 버전이 생기는데, 해당 버전을 **누가 작업을 했느냐에 알기 위해서 이름을 세팅해야한다.**

최초 한번만 하면 되는 작업이고 차후에 변경할 부분이 생길 경우 변경 할 수 있다.

``git config --global user.name`` 명령어를 사용하면 된다.

변경할 요소는 ``name``,``email`` 두가지가 존재한다.

**1.** git username 설정하기

``git config --global user.name``

**2.** git email 설정하기

``git config --global user.email``

**3.** 이제 ``commit`` 명령어를 사용 할 수 있다.

**4.**아래의 명령어를 실행해보자

```git commit```

위의 명령어를 실행하면 텍스트 파일이 하나 열리게 된다. 내부의 내용은 ``git status`` 명령어를 사용할 때 나오는 정보가 출력된다.

아래는 텍스트 파일에 기재되는 정보의 예시이다
```
# 
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch master
# Changes to be committed:
#	modified:   file1.txt
#

```
**5.** commit 완료하기

위의 텍스트 내용을 보면 1번 줄에는 어떤 텍스트도 입력되지 않았다. 해당 라인에 버전 정보를 입력하고 텍스트 파일을 종료하면
이전의 작업했던 것들이 commit 되면서 아래와 같은 정보가 출력된다.
```
[master ba0e788] 1
 1 file changed, 1 insertion(+), 1 deletion(-)
```
이제 commit 이 완료되었다.

**6.** commit 확인하기

commit 이 완료되었는지 확인하기 위해서 다음과 같은 명령어를 실행해본다.
``git log``

해당 명령어를 실행하면 아래와 같은 정보가 출력된다.
```
commit 7cabc955e6f9bf26d8c7bc5e38000f9dc868d21c
Author: tonykrjhc <tonykrjhc@elcompany.kr>
Date:   Tue Dec 6 16:51:33 2022 +0900

    1
```
commit을 누가 했는지와 하단에 표시된 숫자를 통해 버전을 확인 할 수 있다.
**add** 된 파일만이 ``git commit`` 시에 적용된다.










   
   
