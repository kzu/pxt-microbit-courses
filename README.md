# pxt-microbit-courses

Split commits from pxt-microbit for just the courses directory

## updating

```
git fetch microbit
git checkout -b cs-intro microbit/master
git subtree split -P docs/courses -b docs-courses
git checkout master
git rm -rf en
git commit -m "Prepare for update" en
git subtree add -P en docs-courses
git branch -D docs-courses  cs-intro
git push
```