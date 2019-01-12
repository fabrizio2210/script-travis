# script-travis
Collection of script useful with travis

## update-topmodules

It clone the repositories that contain the building project as submodule. It allows to integrate the last commits to other projects that depend on the building project.

It wants two parameters:
- the deploying private key in base64 to push the commits in the repositories to update
- a comma separated list of the repositories with branch and the position of the submodule

The list of the repositories is structrurated as this:
```
<url_project>;<branch>:<path>,<url_project2>;<branch2>:<path2>)
```

Example:
```
./update-topmodules.sh "$MYPROJECT_CI_PRIVATE_KEY" 'https://github.com/fabrizio2210/docker-HA_volume_sync_deployer.git;armv7hf:src'
```
Pay attention to escape the ";"

