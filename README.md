# MergeBranchToMaster

1. Create Branch 
	git branch <branch_name>
	
2. Switch to other branch/master
	git checkout <banch_name/master>
	
		OR
		
	//Create new branch and switch to that branch in one command
	git checkout -b <branch_name>
	
3. Merge branch to master
	git checkout master // switch to master
	git merge <branch_name> //merge file from brach to master
	
4. rebase/update of Master to to branch
	git rebase master  //take update of master repo to branch
	

Example:
		create repo on github
		git clone https://github.com/monu2580/MergeBranchToMaster.git
		cd MergeBranchToMaster
		
		//create new Branch and switch
		git checkout -b b1
		
		mate README.md
			//Do some modifiacation and save
		git commit -m "Commit by branch b1"
		
		//to merge this branch update to mster
		git checkout master
		git merge b1
		git push
		
		mate README.md
			//do some modifiaction
			
		//to get this master modification update to branch b1
		git checkout b1
		git rebase master
		git push
		