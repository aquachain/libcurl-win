# Step by step
1. Clone original repo on github website
2. Checkout cloned repo, add remote to "original" repo
   ```
   git clone https://github.com/huuuus/build-libcurl-windows.git
   git remote add original https://github.com/blackrosezy/build-libcurl-windows.git 
   ```
3. Edit .git/config, to add prs to the "original" remote, by adding this line:
   ```
   fetch = +refs/pull/*/head:refs/remotes/origin/pr/*
   ```
4. Fetch original & checkout the pull request
   ```
   git fetch original
   git branch -a # just to show the available branches
   git checkout remotes/origin/pr/18 .
   ```
# References
* https://gist.github.com/piscisaureus/3342247
