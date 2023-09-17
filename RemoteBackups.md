# Back from remote systems

```bash
#!/bin/bash

dst_svr=missmp@home.sneconsulting.co.uk

weekno=$(date +%U)
week=$(($weekno % 4))

export dst_dir=backups/week${week}/Company

# echo "mkdir ${dst_dir}" | ssh ${dst_svr} 
(export -p; echo  "mkdir -p ${dst_dir}") | ssh ${dst_svr}  'bash -s'

rsync -avzh /e/ServerFolders/Company/* ${dst_svr}:${dst_dir} --exclude=*.bak
```