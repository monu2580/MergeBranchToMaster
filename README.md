# MergeBranchToMaster

1. Create Branch 

		git branch <branch_name>
	
2. Switch to other branch/master
	
		git checkout <banch_name/master>
	
	OR
	
	//Create new branch and switch to that branch in one command
	
		git checkout -b <branch_name>
	
3. Merge other branch to your local branch
	
		git checkout <your_locabranch> // switch to master
		git merge <other_branch> //merge file from brach to master
	
4. rewrite history from other to Your local branch
	
		git rebase <other_branch>  //take update of master repo to branch
	
5. delete branch
	
		git branch -d <branch_name>
Example:
		
		create repo(MergeBranchToMaster) on github
		//create folder(MergeBranchToMaster) in your computer
		cd MergeBranchToMaster
		git init
			OR
		git clone https://github.com/monu2580/MergeBranchToMaster.git
		cd MergeBranchToMaster
		
		//create new Branch and switch
		git checkout -b b1
		
		mate README.md
			//Do some modifiacation and save
		git add README.md
		git commit -m "Commit by branch b1"
		
		//to merge this branch update to mster
		git checkout master
		git merge b1
		git push
		
		mate/gedit README.md
			//do some modifiaction
			
		//to get this master modification update to branch b1
		git checkout b1
		git merge master
		git push
		
		//to reWrit commit and push history of other_branch(master) to local_branch(b1)
		git rebase master
		git push
		
