# lfs

## Find out what files are under LFS
- do a search in folder for .gitattributes
- or do git lfs ls-files


## add files to LFS
https://stackoverflow.com/questions/54451856/how-can-i-tell-if-a-file-will-be-uploaded-to-git-lfs-correctly
1. go to repo and do git lfs install
2. add files to lfs
- git lfs track "*.png" for example to track all files with extension of .png
3. add lfs files
- normal git add process. 
4. view lfs files staged
- git lfs status
5. view lfs files
- git lfs ls-files

## remove files from LFS
- remove hooks
git lfs uninstall
- remove lfs stuff from .gitattributes
- list lfs files using
git lfs ls-files | sed -r 's/^.{13}//' > files.txt
- run git rm --cached for each file
while read line; do git rm --cached "$line"; done < files.txt
- run git add for each file
while read line; do git add "$line"; done < files.txt
- commit everything
git add .gitattributes
git commit -m "unlfs"
git push origin
- check that no lfs files left
git lfs ls-files
- remove junk
rm -rf .git/lfs


https://stackoverflow.com/questions/35011366/move-git-lfs-tracked-files-under-regular-git
https://github.com/git-lfs/git-lfs/issues/3026
