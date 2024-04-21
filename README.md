## Game Dev Fun Size Demo Project

### Prerequisites
- You'll need to have [Rust installed on your machine](https://www.rust-lang.org/tools/install) to run the local git-lfs server.
- You'll need to install git-lfs on your machine as well: `git lfs install`
- Run ` git config lfs.url http://localhost:8080` to set the git-lfs server

I don't love it, but I've had to run:
`git config 'lfs.http://git-server.com/user/test.locksverify' false`
to get around this issue:
> `[::1] POST /api/gdfs/demo-project/locks/verify - 404 Not Found`