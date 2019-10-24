# Cross Cloud CI New Project Gitlab Configuration Setup

# Gitlab Project Configuration #
1. Make crosscloudci/**projectname**-configuration project -- copy an existing **projectname**-configuration project (see testproj-configuration example: https://github.com/crosscloudci/testproj-configuration) 

![test project configuration](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/testproj-configuration.png "testproj configuration")

2. Edit the cncfci.yml (see testproj-configuration: https://github.com/crosscloudci/testproj-configuration/blob/master/cncfci.yml which is for the testproj example: https://github.com/crosscloudci/testproj)

![Test Project](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/testprojectcncfciyml.png "Test Project cncfci.yml YML")

3. Edit .gitlab-ci.yml to include curl commands and scripts for getting build status, deploys, and tests e.g. envoy-configuration (see https://github.com/crosscloudci/testproj-configuration/blob/master/.gitlab-ci.yml)

![Test Project](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/testprojectgitlabyml.png "Test Project gitlab-ci.yml YML")

4. Optional: write a ci proxy plugin for your ci tool and submit a pull request (see https://github.com/crosscloudci/ex_ci_proxy/blob/master/README.md)

## Gitlab Setup
### GitLab Pipeline Setup
***You need to have admin permissions to do this.***
***Also, if this process is done on the production gitlab server, you'll need to rsync the changes to your other servers or implement the same changes manually in each environment.***

In Gitlab you need to complete the following steps.
 1. Create a new group
 
![git add group](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-group.png "gitlab add group")
 
![git add group](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-group-new.png "gitlab add group")
 
 2. Create a new project
 
![git add project](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-project.png "gitlab add project")

![git add project](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-project-new.png "gitlab add project")

 3. Set up mirroring (*steps and menu items in gitlab*)
   - Select admin
   
![git select admin](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-project-admin.png "gitlab select admin")
 
   - Botuser needs to be in user permissions
    
![git select admin](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-manage-access.png "gitlab select admin")
    
     - Add bot user as member (as the master role)
     
![git select admin](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-bot-user.png "gitlab select admin")

   - Impersonate bot user
     - Admin
       - Search for bot, click on bot user

![git search bot user](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-search-bot-user.png "gitlab search bot user")
	    
       - Impersonate bot user
	    
![git impersonate bot user](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-impersonate-bot.png "gitlab impersonate bot user")	    
	    
   - Settings
     - Repository
       - Pull from remote repository
       - Select mirror, add https repo address, select bot user

![git repository mirroring ](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-repository-mirroring.png "gitlab repository mirroring")
	    
   - Select the project Project
        - You should see that the code is pulled down
        
![git check mirroring ](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-check-project-mirror.png "gitlab check mirroring")

        - Stop impersonating the bot user
4. Set up project variables (*steps and menu items in gitlab*)
    - Settings
        - Pipeline trigger

![git add trigger ](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-pipeline-trigger.png "gitlab add trigger")

    - add trigger
    - make sure a token is created
      - Pipelines 
        - Custom ci config path

![git custom path ](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-custom-gitlabciyml.png "gitlab custom path")
	    
          - e.g. https://raw.githubusercontent.com/crosscloudci/envoy-configuration/master/.gitlab-ci.yml
        - Add cloud variable (you only need to add the CLOUD and ARCH variables)

![git add trigger ](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-secrets.png "gitlab add trigger")

          - CLOUD
            - e.g.  aws
          - ARCH
            - e.g. AMD64
5. Enable runners (*steps and menu items in gitlab*)

![git enable runners ](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-enable-runners.png "gitlab enable runners")

    - settings
      - ci/cd
        - Runner settings
          - Enable all runners for this project
6. Add the project to global configuration yml (e.g. https://github.com/crosscloudci/cncf-configuration/blob/master/cross-cloud.yml)

![cross cloud global config](https://github.com/crosscloudci/crosscloudci/blob/master/add-project-cross-cloud-yml.png "cross cloud global config")

    - Cncf configuration
      - Integration branch
        - Add to cross-cloud.yml
          - Duplicate a project
          - Find logo image e.g. https://d33wubrfki0l68.cloudfront.net/77bb2db951dc11d54851e79e0ca09e3a02b276fa/9c0b7/img/envoy-logo.svg
          - Add to cncf artwork repo
            - Link to cross cloud artwork repo
              - Update the project names e.g. to envoy 
              - Charts are the repo that we get the helm charts from
              - Change timeout for how long your build takes
7. Review pipelines

![new pipeline](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-new-pipeline.png "new pipeline")

  - Pipelines
    - manually add new to the url (***this is a workaround***)
      - e.g. https://gitlab.cidev.cncf.ci/envoy/envoy/pipelines/new
        - Select master
        - Select stable (*e.g. v1.7.0*)
        - Both should be running

## Trigger Client
1. Add the new project into the enviroment.rb

![enviroment.rb](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-add-project-enviromentrb.png " environment.rb")

1. Get token from trigger (*steps and menu items in gitlab*)

![.env](https://raw.githubusercontent.com/crosscloudci/crosscloudci/master/gitlab-env.png " .env")

  - Settings
    - Pipeline trigger
      - copy token
    - Put in .env for trigger client

## Optional CI Setup (legacy manual build -- not using ci-proxy )

1.  Clone the project

```
git clone yourprojectname
```	
```
- e.g. git clone https://github.com/envoyproxy/envoy.git
```

2.  Make a note of any ci instructions including
scripts for building and publishing images

- e.g. the .circleci/config.yml file outlines lots of shell scripts
that refer to a docker dependencies image and build image

3. Replicate the builds

- e.g. use docker to replicate a build image using the previously viewed ci 
- you probably want to pin your image
- update the script not to push 
- images will be local after build
- publish to gitlab directory

4. Create a script that builds head 

5. Create a script that builds stable

#### How to Debug
1. Add a sleep to the .gitlab-ci.yml script
2. ssh root@runner.yourgitlaburl
3. Click on compile job

#### Gitlab yml common issues
- If .gitlab-ci.yml does not refresh: 
  - Go to pipelines
  - Copy/cut the gitlab.yml and save an empty url
  - Paste the url in again and save it


