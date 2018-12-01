# strange-merge-sample
This is a sample of `git merge --allow-unrelated-histories` result.
```
cd
rm -rf strange-merge
mkdir strange-merge
cd strange-merge
git init
echo master1 >> master1.txt && git add . && git commit -m "master1"
sleep 1
echo master2 >> master2.txt && git add . && git commit -m "master2"
sleep 1

git checkout --orphan BranchX
echo x1 >> x1.txt && git add . && git commit -m "x1"
sleep 1
echo x2 >> x2.txt && git add . && git commit -m "x2"
sleep 1

git checkout master
git merge --allow-unrelated-histories --no-edit BranchX
sleep 1
```
