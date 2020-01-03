# Jenkins Pipeline

## 1. Checkout from GitHub 

The Checkout plugin has a large variety of Software Configuration Managements (SCMs) available. 

You can check all the avaialble options [here](https://jenkins.io/doc/pipeline/steps/workflow-scm-step/)

To use a specific SCM you can pass it as paramter to `$class` option in the below given snippet.

All the following options and parameters in the checkout step vary depending on the chosen SCM.

We chose to use GitSCM so the below code snippet gives an idea on how to Checkout Code from GitHub and use it as part of your pipeline. 


```groovy

    checkout([
        $class: 'GitSCM', 
        branches: [[name: 'branch_name']], 
        doGenerateSubmoduleConfigurations: false, 
        extensions: [], submoduleCfg: [], 
        userRemoteConfigs: [
            [credentialsId: 'jenkins_credential_id', url: 'git_url']
        ]
    ])

```
#### Brief explanation of the above used options and parameters.

`GitSCM` is the class to be used for Checkout.

`branch_name` is the name of the branch to be checkout out.

`jenkins_credential_id` is the ID of the credential that is configured in Jenkins.

`git_url` is the URL for the git repository.

