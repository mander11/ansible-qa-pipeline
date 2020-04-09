# Ansible QA Pipelines

The goal is to create an easy way incorporate db-snapshots to our product releases

## TODOs

1. Setup ansible locally
2. Have it run against a docker image
3. Ansible will create backup of postgres
4. Ansible copy back to host machine
5. Run docker build and docker push (with pg_dump sql)
6. All of this should run from Jenkinsfile
7.  Repeat for MSSQL (tweaks)

### Setting up ansible locally
My idea: use docker-compose
One image will have ansible control machine
The other will have a simple ssh
This will just be for manual testing.
