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

1. DONE - Setup a docker-compose environment
2. Setup passwordless ssh with redis image
3. Bake it into dockerfile 
4. Hello world playbook
5. Bake hello world playbook into dockerfiles
6. Swap out redis image for postgres
7. Redo hello world playbook with postgres
8. Ansible to create dummy table
9. Ansible to backup schema
10.Ansible to pull back schema

Steps done outside of docker-compose:
1. Run local commands
https://stackoverflow.com/questions/18900236/run-command-on-the-ansible-host
2. Build dockerfile
3. Push to repository
NOTE: will need to setup a dev docker repository
