git init
echo "Initial content" > README.md
git add README.md
git commit -m "Commit 0: Initialize README.md"
echo "Update 1" >> README.md
git commit -am "Commit 1: Update README.md"
echo "Update 2" >> README.md
git commit -am "Commit 2: Further update README.md"
git branch bug-fix
git checkout bug-fix
echo "Bug fix" >> README.md
git commit -am "Commit 3: Apply bug fix"
git checkout master
echo "Feature A" >> README.md
git commit -am "Commit 10: Add feature A"
git checkout bug-fix
echo "Improvement to bug fix" >> README.md
git commit -am "Commit 4: Improve bug fix"
echo "Refactoring" >> README.md
git commit -am "Commit 5: Refactor code"
git checkout master
echo "Feature B" >> README.md
git commit -am "Commit 11: Add feature B"
git checkout bug-fix
echo "Bug fix enhancement" >> README.md
git commit -am "Commit 6: Enhance bug fix"
git checkout master
git merge bug-fix --no-ff -m "Commit 12: Merge bug-fix into master with conflict resolution"
git add README.md
git commit -m "Commit 12: Merge bug-fix into master with conflict resolution"
git checkout bug-fix
git branch bug-fix-experimental
git checkout bug-fix-experimental
echo "Experimental fix" >> README.md
git commit -am "Commit 7: Experimental fix"
echo "More experimental work" >> README.md
git commit -am "Commit 8: More experimental work"
echo "Finalize experiment" >> README.md
git commit -am "Commit 9: Finalize experiment"
git checkout bug-fix
git merge bug-fix-experimental --no-ff -m "Commit 13: Merge bug-fix-experimental into bug-fix"
git checkout master
git merge bug-fix --no-ff -m "Merge bug-fix into master"
# Image made here, README.md modified
git add README.md commit_graph.png
git commit -m "Commit 14: Add README.md and commit graph image"
