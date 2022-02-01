# Annotations
Annotations: Some commands to remember since I'm getting old, as well as my friends who can relly on this!


## git

### Create branch local and remote
```
git pull -v
git checkout -b feature/newfeature
git push --set-upstream origin feature/newfeature
```

### Remove branch local, origin and remote
```
git branch -d [name_of_your_new_branch] # removes local copy of branch OR
git branch -D [name_of_your_new_branch] # removes local copy of branch
git branch -rd origin/[name_of_your_new_branch] # removes local copy of origin branch
git push origin :[name_of_your_new_branch]  # removes remote branch
```

## Ansible

 [Ansible.md](https://github.com/mariomelofilho/annotations/blob/master/Ansible.md)

