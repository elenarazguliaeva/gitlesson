# gitlesson
1. Create github repo.
2. Create directory, init git repo and create three files
mkdir /tmp/gitlesson
cd /tmp/gitlesson
git init
echo "first file to commit" > first.txt
echo "second file to commit" > second.txt
echo "third file to commit" > third.txt
3. Stage and commit.
git add *
git commit -m "three new files"
4. Create two new branches, make changes in them.
git checkout -b firstbranch
nano first.txt
git add *
git commit -m "first branch changes"
git checkout master
git checkout -b secondbranch
nano second.txt
git add *
git commit -m "second branch changes"
5. Merge one branch into another.
git merge firstbranch
6. Merge current branch into master
git checkout master
git merge secondbranch
7. Revert last commit
git reset --hard HEAD~1
8. Push all changes to git repo.
git remote add origin git@github.com:elenarazguliaeva/gitlesson.git
git config --global user.email "elena.razgulayeva@gmail.com"
git config --global user.name "Elena Razguliaeva"
git push --set-upstream origin master

git checkout firstbranch
git push --set-upstream origin firstbranch
git checkout secondbranch
git push --set-upstream origin secondbranch
