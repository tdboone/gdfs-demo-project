## Game Dev Fun Size Demo Project

### Prerequisites
- You'll need to have [Rust installed on your machine](https://www.rust-lang.org/tools/install) to run the local git-lfs server.
- You'll need to install git-lfs on your machine as well: `git lfs install`

### Getting Started
- Run `$ export GIT_LFS_SKIP_SMUDGE=1` to prevent git from trying to download lfs files when cloning
- Run `git clone --recursive https://github.com/tdboone/gdfs-demo-project.git` to clone the repository
- Open lfs-server.sh.template, add your AWS credentials for the project's lfs bucket, and then *save as* lfs-server.sh (this file is on the .gitignore to prevent you from accidentally commiting your credentials.)
