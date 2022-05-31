Implementation Repo
-------------------

This repository is intended to deploy and configure the [solution repository](https://github.com/adrime92/halborn-assestment-solution) in different environemnts.


How to use it
-------------------
1. Create a new branch e.g.: ```feature/deploy-v.1.0.0```, fill up the configuration files, both in ```prod/group_vars/all/``` and ```stg/group_vars/all/```, also fill up the terraform vars in ```var.tf```. You can get some info about the needed variables from [README.md](https://github.com/adrime92/halborn-assestment-solution/blob/master/README.md#variables) 
2. In the ```requirements.yml``` files ```prod/requirements.yml``` and ```stg/requirements.yml``` specify the solution's desired release to be deployed. Check available releases here: [releases](https://github.com/adrime92/halborn-assestment-solution/tags)
3. Create a commit and push it, it will trigger the ```.gitlab-ci.yml``` pipeline and will deploy the stg environment gathering the configuration files from the stg folder.
4. If everything runed smoothly, make a PR to master. Once you merge in master the PR will run again and will gather the configuration files from the prod folder.
