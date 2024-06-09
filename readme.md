
### enlever le dernier commit et le garder en stage
git reset HEAD~1

### supprimer le dernier commit 
git reset --hard HEAD~1

### fusionner une autre banch avec ma branch locale
git checkout main
git merge preprod

### ajouter un commit qui annule un autre commit
git log
git revert <commit-hash>


### fusionner des branch merge ou rebase

git fetch origin main
git merge main

git fetch origin main
git rebase main

git pull origin <branch-name>

git merge --abort
git rebase --abort

git config --global --get pull.rebase
git config --list

### avec rebase il faut récrire l'historique
git push origin preprod --force-with-lease


### fast forward
fast forward quand vous travaillez sur une branche, disons feature, et que personne d'autre n'a fait de commit sur la branche main pendant ce temps. Lorsque vous fusionnez votre branche feature dans main, Git peut simplement déplacer le pointeur de main vers le dernier commit de feature. C'est ce qu'on appelle un "fast-forward".

### rebase interactif 
git log 
git rebase -i HEAD~n

p, pick : utiliser le commit
r, reword : utiliser le commit, mais modifier le message de commit
e, edit : utiliser le commit, mais arrêter pour modifier le commit
s, squash : utiliser le commit, mais fusionner dans le commit précédent
f, fixup : comme "squash", mais jeter le message de commit
d, drop : supprimer le commit


### rebase interactif edit de commit workflow
git log 
git rebase -i HEAD~n


pick commitid -> e
modif de fichier
git add .
git commit --amend
git rebase continue



### rebase interactif ajouter des fichier
git add forgotten-file.txt
git commit --amend


### voir un commit 
git show COMMIT_ID



