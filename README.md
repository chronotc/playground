# playground

expected hash where diverted branched off master

branch-a  = f2729bc8ef7faba4f6b90c3cd9219180443f7c21 (first commit on master) <-- we want this
          = 6d3e61bc92bf79eacc8444e5afc634908ccdc9fd (where master was merged)
branch-b  = f2729bc8ef7faba4f6b90c3cd9219180443f7c21 (first commit on master) <-- we want this
branch-c  = 45ed4e64fcab7e3b93d3c32e74e7df607304bc16 (where branch-c branches off branch-a) <-- we want this
branch-d  = 92ebad06085de2261873dcffa47fc560a2609a15 (this was rebased) <-- we want this


Solution #1

`git merge-base master <branch-name>`

Has issues with intermediate merges as it will take the latest merge commit on the branch. This works fine if people rebase (make it as part of workflow)