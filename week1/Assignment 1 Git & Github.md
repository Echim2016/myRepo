# Assignment 1: Git & Github




#### <code class="highlighter">git status</code>

本指令用來檢視當前資料夾的狀態，常用於檢視資料夾中的檔案有哪些新的變更，或者檢查工作區（Working Directory）是否已清空。

#### 使用情境舉例：編輯README檔案後，用<code class="highlighter">git status</code>來檢視新的變更。

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

本指令用來將檔案從工作區（Working Directory）移至暫存區（Staging Area），這個指令會讓 git 得以開始追蹤這個檔案，使其成為後續可以commit的檔案。

#### 使用情境舉例：編輯README檔案後，用<code class="highlighter">git add</code>將檔案移至暫存區（Staging Area）。

```
$ vim README.md
$ git add README.md 
```
<br>


---

### 如何部署 GitHub Repository？ 


### 如何上傳本地專案資料夾（Local Project）？

