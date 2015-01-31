# rublog
procedure to create github pages only branch:

1. Create repository in github
2. Create new branch called gh-pages from master: ![gh-pages create](https://pages.github.com/images/create-branch@2x.png)
3. Clone repository with only one branch by
	
	git clone -b gh-pages --single-branch git@github.com:famer/rublog.git 

4. Create new jekyll site with same name. User --force to put it there
		
	jekyll new rublog --force

After that you will have dir called as your repository with only one branch `gh-pages` and all remotes configured.

After that use usual:
	
	git add --all
	git commit -m "init"
	git push


Optionally you can make gh-pages default branch for you repository:
![gh-pages default branch](https://pages.github.com/images/default-branch@2x.png)
