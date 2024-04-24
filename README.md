## Game Dev Fun Size Demo Project

### Prerequisites
- You'll need to have [Rust installed on your machine](https://www.rust-lang.org/tools/install) to run the local git-lfs server.
- [Install git](https://git-scm.com/downloads) if you haven't already and you'll need to install git-lfs on your machine as well: `git lfs install`
- This project runs Unreal Engine 5.3, so [you'll need that installed](https://www.unrealengine.com/en-US/download) to open the project.

### Getting Started
- Run `$ export GIT_LFS_SKIP_SMUDGE=1` to prevent git from trying to download lfs files when cloning
- Run `git clone --recursive https://github.com/tdboone/gdfs-demo-project.git` to clone the repository (including a submodule that implements a local git-lfs server)
- Open lfs-server.sh.template, add your AWS credentials for the project's lfs bucket, and then *save as* lfs-server.sh (this file is on the .gitignore to prevent you from accidentally commiting your credentials.)
- From within the project root, run `$ ./lfs-server.sh` to start the local lfs server, "Rudolfs". This will need to be running any tme you pull from or push to the repo to sync binary files to the s3 bucket.
- Run `$ export GIT_LFS_SKIP_SMUDGE=0` to tell git to automatically pull and clone lfs files from now on
- Run `$ git lfs pull` to download the missing lfs files
- Open the .uproject file and make sure the game project opens correctly