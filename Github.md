## 1.文件传输   
----  
>1.强烈建议先在本地创建或修改文件，在push到github上。  
>2.若是Repositry，先在github上创建，在clone到本地。  

### Github >> 本地:
  
    git reset --hard  
    git pull

### 本地 >> Github(包含新建文件夹或修改旧的文件):

    git add file.md  
    git commit -m "tittle"  
    git push  

#### push 不成功(或者先pull再push):
    因为githun中的Readme.md文件不在本目录中  
    git add  
    git commit -m "tittle"  
    git pull --rebase origin master  
    git push -u origin master
    之后就可以直接push了

----
### Repository >> 本地:  
    1. 生产SHH Key:直接输入'ssh',如有提示，说明已安装。  
    紧接着输入'ssh-keygen -t rsa',连续三个回车（不要输入密码）,然后会在user文件夹中生产个.ssh文件夹(包含3个文件)。  
    前往Github,依次'setting >SSH Keys >New SHH Key'。  
    Tittle处写'id rsa.pub',再把'id rsa.pub'里的内容复制进去。  
    SHH Keys添加成功后，输入'ssh -T git@github.com'进去测试  

    2. git clone+地址(Repo那有)。

### 本地 >> Repository:
    新建文件夹，新建文件（git bash here)  
    git init  
    git add  
    git commit -m "initial commit"  
    git remote add origin （地址）  
    git push origin master

#### 新建文件2如何push?

    git add 'file'  
    git commit -m "new"  
    git push  

----

## 2.文件删除
------
### 删除本地文件:
    分两种情况：  
    1. 在本地新建的,且已经push到Repo:  
    在本地先删除，再去Repo删除   
  
    git status
    git rm 'file'  
    git commit -m 'rm'
    
    2. 在Repository新建的,且已经pull到本地:   
    不管先在本地还是在Repo删除，效果一样
    
    

### 删除Repository文件:
    不管先在本地还是在Repo删除，效果一样    

    git status
    git rm 'file'  
    git commit -m 'rm'
