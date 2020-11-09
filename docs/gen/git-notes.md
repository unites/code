# Git && Github

## Add acount


```sh
# Enable only for current repo
git config credential.helper store
git config user.name 
git config user.email 

# Enable Global
git config --global credential.helper store
git config --global user.name 
git config --global user.email 
```

```sh
git add .
git commit -m "update notes"
git push origin
git subtree push --prefix site origin gh-pages

# Or all together

git add . && git commit -m "notes" && git push origin && git subtree push --prefix site origin gh-pages

```