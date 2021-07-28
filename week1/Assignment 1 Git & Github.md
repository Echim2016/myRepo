# Assignment 1: Git & GitHub


#### Q1. Please apply for a GitHub account and create a repository then upload your homework to the repository.

```
// GitHub repository link as below:

https://github.com/Echim2016/remote-assignment
``` 
<br>
<br>



#### Q2. Here are a few git and GitHub commands we usually use in software development, please explain the meanings and use cases of them.
<br>

#### <code class="highlighter">git status</code>

本指令用來檢視當前資料夾的狀態，常用於檢視資料夾中的檔案有哪些新的變更，或者檢查工作區（Working Directory）是否存在未追蹤的檔案。

##### 使用情境舉例：編輯README檔案後，用<code class="highlighter">git status</code>來檢視新的變更。

```
$ vim README.md
$ git status

 On branch master
 Your branch is up to date with 'origin/master'.

 Changes not staged for commit:
   (use "git add <file>..." to update what will be committed)
   (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

 no changes added to commit (use "git add" and/or "git commit -a")
``` 
<br>


#### <code class="highlighter">git add</code>

本指令用來將檔案從工作區（Working Directory）移至暫存區（Staging Area），這個指令會讓 git 得以追蹤這個檔案，使其成為後續可以提交（Commit）的檔案。

##### 使用情境舉例：編輯README檔案後，用<code class="highlighter">git add</code>將檔案移至暫存區（Staging Area）。

```
$ vim README.md
$ git add README.md 
```
<br>

#### <code class="highlighter">git commit</code>

本指令用來將檔案從暫存區（Staging Area）移至儲存庫（Repository），讓檔案能確實被存在本地儲存庫裡，每一次的提交（Commit）也是一個專案當下狀態的快照（Snapshot），使開發者後續能向前回溯不同版本的進度。

##### 使用情境舉例：編輯README檔案後，用<code class="highlighter">git commit</code>將檔案移至儲存庫（Repository），並留下本次編輯內容的提交訊息紀錄。

```
$ vim README.md
$ git add README.md 
$ git commit -m "Adding new project information"
```
<br>

#### <code class="highlighter">git log</code>

本指令用來顯示 Repository 先前所有提交（commit）的紀錄，每一次的提交紀錄，會顯示 commit 的 hash 碼、作者、提交時間、提交訊息等內容。

##### 使用情境舉例：在完成幾次提交（Commit）之後，用<code class="highlighter">git log</code>查詢歷史提交紀錄。

```
$ git log

 commit 600e0bb65608693f03fae8e71982b736ee2405e5 (HEAD -> master)
 Author: Echim2016 <......@gmail.com>
 Date:   Tue Jul 27 19:26:41 2021 +0800

     Adding new project information

 commit 9c8c26474595d8fd01279f2fca4e0589c42859ae  (origin/master)
 Author: Echim2016 <......@gmail.com>
 Date:   Tue Jul 27 11:20:44 2021 +0800

     Initial commit
```
<br>

#### <code class="highlighter">git push [ Repo_name ] [ Branch_name ]</code>

本指令用來將本地的分支（Branch）推送到遠端的儲存庫（Repository），並在遠端建立同樣名為 [ Branch_name ] 的分支。

##### 使用情境舉例：在本地完成更改後，用<code class="highlighter">git push origin master</code>將本地檔案推送到遠端儲存庫（Remote Repository）。

```
$ git push origin master

 Enumerating objects: 9, done.
 Counting objects: 100% (8/8), done.
 Delta compression using up to 4 threads
 Compressing objects: 100% (4/4), done.
 Writing objects: 100% (5/5), 583 bytes | 583.00 KiB/s, done.
 Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
 remote: Resolving deltas: 100% (1/1), done.
 To https://github.com/Echim2016/myRepo.git
    b7cfe84..be93497  master -> master
```
<br>

#### <code class="highlighter">git remote -v</code>

本指令用來顯示目前連結本地專案的遠端儲存庫(Remote Repository)及對應的URLs。


##### 使用情境舉例：用<code class="highlighter">git remote -v</code>查詢當前與本地專案連結的遠端儲存庫。

```
$ git remote -v

  origin	https://github.com/Echim2016/myRepo.git (fetch)
  origin	https://github.com/Echim2016/myRepo.git (push)
```
<br>

#### <code class="highlighter">git branch</code>

本指令用來顯示儲存庫（Repository）當下的所有分支（Branch）。


##### 使用情境舉例：在新增一個bugFix分支後，用<code class="highlighter">git branch</code>查詢目前儲存庫（Repository）的所有分支（Branch）。

```
$ git branch bugFix        #新增一個除錯用的分支
$ git branch

    bugFix
  * master
```
<br>

#### <code class="highlighter">fork</code>

fork 並非一種 git 指令。此動作意指開發者在 GitHub 上快速複製（Fork）一個他人的儲存庫（Repository），並將其建立在自己的遠端儲存庫（Remote Repository）之下。開發者此時即能自由讀寫內容，並能在修改後，對原開發者發送 Pull Request，讓變更得以重新合併，完成專案的多人協作。

##### 使用情境舉例：在GitHub上針對一個開源的專案（圖中以新台語運動 iTaigi為例），點擊<code class="highlighter">fork</code>即可複製一份副本到自己的遠端儲存庫（Remote Repository）。

![](https://i.imgur.com/UNetsFM.png)

##### 使用情境舉例：在個人的遠端儲存庫（Remote Repository）可見 iTaigi 專案已成功複製，且能看見其原始來源。
![](https://i.imgur.com/0Txlmkq.png)

<br>
<br>





#### Q3. Please describe how to establish a GitHub repo and how to upload the local projects to GitHub. Try to explain your answers with as much detail as possible.
<br>

### 如何部署 GitHub Repository？ 

1. 進入 GitHub 首頁，點擊右上角的「＋」，點選 **「New Repository」**。

![](https://i.imgur.com/u9VyuKA.png)

2. 填入 *Repository Name* 以及 *Description*，點擊 **「Create Repository」** 。

![](https://i.imgur.com/eHWDu6p.png)


3. 完成 Github Repository 基本部署。

![](https://i.imgur.com/Gw4b8J2.png)


<br>

### 如何上傳本地專案資料夾（Local Project）？


1. 複製 GitHub Repository 頁面中 Quick Setup 的 HTTPS 連結：
```
https://github.com/Echim2016/demoRepo.git
```
 
2. 進到本地專案資料夾，並以 <code class="highlighter">git init</code> 進行初始化。
```
$ cd demoRepo
$ git init
```
3. 以 <code class="highlighter">git remote</code> 進行遠端儲存庫（Remote Repository）連結。

```
# 輸入 git remote add origin [Your Quick Setup HTTPS URL]

$ git remote add origin https://github.com/Echim2016/demoRepo.git
```

4. 以 <code class="highlighter">git push</code> 將本地專案資料夾的檔案推送至遠端儲存庫（Remote Repository）中。

```
$ git push --set-upstream origin master
```

5. 後續本地專案資料夾中的檔案更動，可利用 <code class="highlighter">git add</code>、 <code class="highlighter">git commit</code>、 <code class="highlighter">git push</code> 等方式進行檔案的同步與上傳。以下以編輯 <code class="highlighter">README.md</code>為例。

```
$ vim README.md
$ git add README.md
$ git commit -m "Initial commit of readme.md"
$ git push origin master
```


6. 回到 GitHub Repository 頁面，可見 <code class="highlighter">README.md</code> 已成功上傳。

![](https://i.imgur.com/XjMgEyc.png)

<br>
<br>

> [2021-07-27 21:31 Yi-Chin Hsu]