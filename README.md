<pre>
 
 --------------
| EXERCICIO01 |
 --------------
Vinicius Menezes da Silva
RA 2402039


<b>A) No working dir, executar o comando: echo 01 > arquivo.txt</b>
    @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 01 > arquivo.txt

 
<b>B) Adicionar o arquivo no staging e conferir o status</b>
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
  On branch main

  No commits yet

  Changes to be committed:
    (use "git rm --cached <file>..." to unstage)
          new file:   arquivo.txt
     
<b>C) Commitar o arquivo do staging com a descrição "git add example - arquivo.txt“</b>
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "git add example - arquivo.txt"
  [main (root-commit) 9a6a39e] git add example - arquivo.txt
   1 file changed, 1 insertion(+)
   create mode 100644 arquivo.txt

     
<b>D) Sobrescrever o conteúdo do arquivo.txt: echo 02 > arquivo.txt</b>
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 02 > arquivo.txt

     
<b>E) Verificar o diffing no arquivo</b>
 @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff
  diff --git a/arquivo.txt b/arquivo.txt
  index 8a0f05e..9e22bcb 100644
  --- a/arquivo.txt
  +++ b/arquivo.txt
  @@ -1 +1 @@
  -01
  +02

     
<b>F) Adicionar novamente o arquivo no staging e conferir o status</b>
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
  On branch main
  Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
          modified:   arquivo.txt

     
<b>G) Verificar o diffing no arquivo</b>
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff arquivo.txt

     
<b>H) Sobrescrever o conteúdo do arquivo.txt: echo 03 > arquivo.txt</b>
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 03 > arquivo.txt

     
<b>I) Verificar o diffing no arquivo</b>
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff arquivo.txt
  diff --git a/arquivo.txt b/arquivo.txt
  index 9e22bcb..75016ea 100644
  --- a/arquivo.txt
  +++ b/arquivo.txt
  @@ -1 +1 @@
  -02
  +03

     
<b>J) Fazer o restore do arquivo da área de staging e verificar o status</b>
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git restore --staged arquivo.txt
  @ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
  On branch main
  Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
          modified:   arquivo.txt

  no changes added to commit (use "git add" and/or "git commit -a"

   
<b>K) Realizar o commit do arquivo e verificar o log</b>
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt 
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m arquivo.txt
[main c85ebfc] arquivo.txt
 1 file changed, 1 insertion(+), 1 deletion(-))

@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git log
commit f479d07ab63f847837d53b15e7cef70b49b29840 (HEAD -> main)
Author: Vinicius Menezes da Silva <vinicius.menezes@aluno.faculdadeimpacta.com.br>
Date:   Wed Aug 14 17:04:47 2024 +0000

    .

commit c85ebfcfcaecb390e60bffaad4fc41785b738589
Author: Vinicius Menezes da Silva <vinicius.menezes@aluno.faculdadeimpacta.com.br>
Date:   Wed Aug 14 16:58:25 2024 +0000

    arquivo.txt


   
<b>L) Adicionar um arquivo gitignore com o seguinte conteúdo: *.txt</b>
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ vi .gitignore
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ cat .gitignore 
*.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add .gitignore
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore

@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m .
[main f479d07] .
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
nothing to commit, working tree clean
  
<b>M) Criar um arquivo novo.txt e verificar o status</b>
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo > novo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ ls
arquivo.txt  novo.txt


     ------------------------------
| - Output de toda a atividade: |
 ------------------------------

@ViniSilvaImpacta ➜ /workspaces/codespaces-blank $ git config --global user.name "Vinicius Menezes da Silva"
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank $ git config --global user.email "vinicius.menezes@aluno.faculdadeimpacta.com.br"
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank $ mkdir exercicio01
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank $ cd exercicio01/
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 $ ls
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 $ git init
Initialized empty Git repository in /workspaces/codespaces-blank/exercicio01/.git/
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ ls
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ cd .git/
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01/.git (main) $ ls
HEAD  branches  config  description  hooks  info  objects  refs
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01/.git (main) $ ls -a
.  ..  HEAD  branches  config  description  hooks  info  objects  refs
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01/.git (main) $ git status
fatal: this operation must be run in a work tree
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01/.git (main) $ cd ..
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 01 > arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   arquivo.txt

@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m "git add example - arquivo.txt"
[main (root-commit) 9a6a39e] git add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 02 > arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo 03 > arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git restore --staged arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git diff
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+03
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m arquivo.txt
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add arquivo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m arquivo.txt
[main c85ebfc] arquivo.txt
 1 file changed, 1 insertion(+), 1 deletion(-)
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ vi .gitignore
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo > novo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m .
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git add .gitignore
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore

@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git commit -m .
[main f479d07] .
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
nothing to commit, working tree clean
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ echo "EXERCÍCIO 01" > README.md
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git log
commit f479d07ab63f847837d53b15e7cef70b49b29840 (HEAD -> main)
Author: Vinicius Menezes da Silva <vinicius.menezes@aluno.faculdadeimpacta.com.br>
Date:   Wed Aug 14 17:04:47 2024 +0000

    .

commit c85ebfcfcaecb390e60bffaad4fc41785b738589
Author: Vinicius Menezes da Silva <vinicius.menezes@aluno.faculdadeimpacta.com.br>
Date:   Wed Aug 14 16:58:25 2024 +0000

    arquivo.txt

commit 9a6a39e8d3277c816beb5484c50f2851f78e34b6
Author: Vinicius Menezes da Silva <vinicius.menezes@aluno.faculdadeimpacta.com.br>
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ cat .gitignore 
*.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ git status
On branch main
nothing to commit, working tree clean
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ ls
arquivo.txt  novo.txt
@ViniSilvaImpacta ➜ /workspaces/codespaces-blank/exercicio01 (main) $ 

</pre>
