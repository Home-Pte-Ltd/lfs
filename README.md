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
1. remove what ever extension or files that was previously tracked as LFS file in .gitattritbutes
2. view "changed files from LFS to normal files". git lfs status
3. git add, commit and push to git server
- You can check in Github, the files are not stored in Github LFS server. 
