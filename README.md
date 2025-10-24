# cherrypick_practice

Task4: Cherry-pick Practice
•       Create repo cherrypick_practice.
•       Create a branch featureA and make 3 commits.
•       Switch to main and cherry-pick only the 2nd commit from featureA.
•       Verify using git log that only that commit was added.
•       Push to GitHub and share screenshots of logs before & after cherry-pick.

The steps followed are :
1. create a new repository on github and clone it to the local machine as cherrypick_practice
   git clone <code>

2.Create a new file and make initial commit
  echo "Initial commit" > demo.txt
  git add demo.txt
  git commit -m "Initial commit"

3.Create and switch to a new branch featureA
  git checkout -b featureA

4.Make 3 commits on featureA
  echo "Feature A - change 1" >> demo.txt
  git add demo.txt
  git commit -m "FeatureA: Commit 1"

  echo "Feature A - change 2" >> demo.txt
  git add demo.txt
  git commit -m "FeatureA: Commit 2"

  echo "Feature A - change 3" >> demo.txt
  git add demo.txt
  git commit -m "FeatureA: Commit 3"
  to verify: git log --oneline

5.Switch back to main branch
  git checkout main

6.Cherry-pick only the 2nd commit
  git cherry-pick <commit hash>
  This will apply only the 2nd commit from featureA onto main.

7.Verify using git log
  git log --oneline --graph

8.Push to GitHub
  git push -u origin main
  git push origin featureA

